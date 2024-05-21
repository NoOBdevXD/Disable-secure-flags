# Disable Secure Screenshot Miui/HyperOs


### Instructions
Need Basic Knowledge To Modify Jar

### Needed Files
- [MT Manager](https://t.me/mtmanager) 

- services.jar & miui-services.jar


### In services.jar
- search method:- isScreenCaptureAllowed

Now replace whole method:-
```
.method public isScreenCaptureAllowed(I)Z
   .registers 4

   const/4 v0, 0x1

  return v0  
.end method
```

### Next
- search method:- getScreenCaptureDisabled

Now replace whole method:-
```
.method public getScreenCaptureDisabled(Landroid/content/ComponentName;IZ)Z
    .registers 5

    const/4 v0, 0x1

    return v0
.end method
```

### Next
- search method:- SetScreenCaptureDisabled

Now replace whole method:-
```
.method private setScreenCaptureDisabled(I)V
    .registers 6

    return-void
.end method
```

### Next
- search method:- isSecureLocked

Now replace whole method:- isSecureLocked
```
.method isSecureLocked()Z
    .registers 6

    const/4 v0, 0x0

    return v0
.end method
```

### Next
- search method:- setSecure

Now replace whole method:-
```
.method setSecure(Z)V
    .registers 14

    return-void
.end method
```


# Miui User Skip this
- Now in miui-services.jar

- search method:- notAllowCaptureDisplay

Now replace whole method:-
```
.method public notAllowCaptureDisplay(Lcom/android/server/wm/RootWindowContainer;I)Z
    .registers 9

    const/4 v0, 0x0

    return v0
.end method
```

### Done 
