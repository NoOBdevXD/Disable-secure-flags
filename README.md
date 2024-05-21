# Disable Secure Screenshot Miui/HyperOs


### Instructions
Need Basic Knowledge To Modify Jar

### Needed Files
- [MT Manager](https://t.me/mtmanager) 

- services.jar & miui-services.jar


### In services.jar
search method:- isScreenCaptureAllowed

Now replace whole method:-
```
.method public isScreenCaptureAllowed(I)Z
   .registers 4

   const/4 v0, 0x1

  return v0  
.end method
```



