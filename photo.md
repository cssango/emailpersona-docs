# Photo


This method allows you to get the profile photo for an email address. 
```
https://api.emailpersona.net/photo/{email}
```

This will return `128x128` pixel image. The available sizes are `64`, `128`, `256`, `512`

You can specify the size like this:

```
https://api.emailpersona.net/photo/{email}?size={size}
```
**Note:** When you specify a size, it must be one of the available sizes, otherwise, the default size of 128px will be returned.

You can place this URL as the `src` attribute of your images like this: 

```html
<img src="https://api.emailpersona.net/photo/{email}?size={size}" />
```
