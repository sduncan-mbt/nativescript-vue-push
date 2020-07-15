<!-- @format -->

<template>
  <Page>
    <ActionBar title="Welcome to NativeScript-Vue!" />
    <ScrollView>
      <StackLayout>
        <Button text="Check Enabled" @tap="checkEnabled" />
        <Label :text="isCheckEnabled" textWrap="true" />
        <Button text="Register" @tap="registerNotifications" />
        <TextView :text="notificationToken" editable="true" />
        <Button text="Get Token" @tap="getToken" />
        <TextView :text="regToken" editable="true" />
      </StackLayout>
    </ScrollView>
  </Page>
</template>

<script>
const messaging = require("nativescript-push");
export default {
  data() {
    return {
      isCheckEnabled: false,
      regToken: "",
      notificationToken: "",
    };
  },
  methods: {
    checkEnabled() {
      this.isCheckEnabled = messaging.areNotificationsEnabled();
    },
    async registerNotifications() {
      this.notificationToken = await messaging.registerForPushNotifications({
        onPushTokenReceivedCallback: (token) => {},
        onMessageReceivedCallback: (message) => {},
        showNotifications: true,
        showNotificationsWhenInForeground: true,
      });
    },
    async getToken() {
      this.regToken = await messaging.getCurrentPushToken();
    },
  },
};
</script>

<style scoped>
ActionBar {
  background-color: #53ba82;
  color: #ffffff;
}
</style>
