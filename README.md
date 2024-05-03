** A repo built from following guide from [JS Mastery](https://github.com/adrianhajdin/aora)**

Prequiste
---
Have [node](https://nodejs.org/en) installed

Run the following command in terminal

1.
```
npx create-expo-app my-app
```
you can modify `my-app` to change the name of the project

2.

```
npm install appwrite@14.0.1
```

   

Frontend built in React-Native
---
There are 3 main routes for users to navigate, which are Home, create and profile.
1. Home page will render the trending video both horizontally and vertically. (Although currently there are no videos as no one using the app)
2. Create page will let user to upload the video with thumbnail, title and description (which is directly stored in the database created by Appwrite)
3. Profile page will display the user info, such as follower(the follower function is currently not implemented) and the numbers of video they uploaded.

Backend managed by [Appwrite](https://appwrite.io/)
---
1. Follow the instructions on the webpage and register
2. Login and create project
3. Create a database
4. Create two collections (in this example the collection ID would be users and video)
5. Within the video collection ID go to attributes and create 5 attributes
6. The attributes for video collection ID:

| Key | Type | Required |
| -------- | ------- | ------- |
| Title | string | Yes |
| thumbnail | url | Yes |
| prompt | string | Yes |
| Video | url | Yes |
| creator | relationship | Yes |

7. Within the users collection ID and create 4 attributes
8. The arrributes for users collection ID:

| Key | Type | Required | 
| -------- | ------- | ------- | 
| user | string | Yes |
| email | email | Yes |
| avatar | url | Yes |
| account ID | string | Yes |

9. Additional backend logic are located in the `Appwrite.js` file and `useAppwrite.js` file in this repo



CI/CD by [expo](https://expo.dev/)
---

running the app in dev mode
```
npx expo start
```
