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
key=lostOFchars

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

