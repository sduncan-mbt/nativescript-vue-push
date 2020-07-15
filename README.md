# NativeScript-Vue-push

> NativeScript-Vue Application using nativescript-push

POST
https://fcm.googleapis.com/fcm/send

application/json
{
  "notification": {
    "title": "Test Push notification",
    "body": "Hello App"
  },
  "to": "UUID"
}

Authorization
key=AAAAg83TGlY:APA91bGxqzt8UTz1vzKDbofMCd0J75H4e5sFj2ft4chZBr9loIlA8EK0jd6Sz1BfMTEAFnMUniKMwhXCgKoizlF8hxWgcJwkwbcRXHmyZO9dvZZuFu5TyCLsmQCXH_XPwI0VPomdlZrX

## Usage

``` bash
# Install dependencies
npm install

# Preview on device
tns preview

# Build, watch for changes and run the application
tns run

# Build, watch for changes and debug the application
tns debug <platform>

# Build for production
tns build <platform> --env.production

```

