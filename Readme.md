## web2py

### Download pinpoint-py-plugins
[pinpoint-py-plugins](https://github.com/pinpoint-apm/pinpoint-c-agent/releases/download/V2020.12.17/pinpoint-python-plugins-v0.0.1.tar.gz)


### Steps
1. copy pinpoint
2. enable pinpoint middleware
    ```py
    def run(servername, ip, port, softcron=True, logging=False, profiler=None,
        options=None):
        ...
        ## import pinpoint middleware
        from pinpoint.pyweb2.middleware import PinPointMiddleWare
        application = PinPointMiddleWare(application)
        getattr(Servers, servername)(application, (ip, int(port)), options=options)
    ```

3. run "python anyserver.py"

