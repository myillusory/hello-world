    req = urllib.request.Request(url,
                                 data,
                                 headers,
                                 method="POST")

    response = urllib.request.urlopen(req)
    info = response.read().decode("utf-8")
    #print(info)


    # json decode: json str --> dict
    jsonLoads = json.loads(info)
    print(jsonLoads['translateResult'][0][0]["src"])
    print(jsonLoads['translateResult'][0][0]["tgt"])
