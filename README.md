# URL-to-SmartJourney

1. To Website: https://smartjourney.fun

(Note: Our server is set up in Hong Kong. Therefore, if you access it from other continents, the loading might be slow.)

**You can use this default account to login in admin interface:**
```
User: admin
Password: admin
```
\
2. To Travel Assistant: http://8.134.253.199:8080/ui/chat/fdaa7d1c95daf74c

# If you find your Travel Assistant can not work when you deploy on your localhost
## 1. Find frontend/src/App.vue
![image](https://github.com/user-attachments/assets/b96332a4-c955-42c1-98a1-4c8dfb78f711)
## 2. Replace line 20~30 to
```html
<template>
  <div>
    <router-view/>
    <ChatbotWidget
      v-if="showChatbot"
      protocol="http"
      host="8.134.253.199:8080"
      token="fdaa7d1c95daf74c"
    />
  </div>
</template>
```
