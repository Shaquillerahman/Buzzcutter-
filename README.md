# Buzzcutter-
Haircuts app
npx create-expo-app buzzcutter
cd buzzcutter
npm install firebase expo-location react-navigation react-native-maps @react-native-async-storage/async-storage
/buzzcutter
  /screens
    LoginScreen.js
    HomeScreen.js
    RequestCutScreen.js
    TrackingScreen.js
  /services
    firebase.js
    barberService.js
    paymentService.js
App.js
import { initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";
import { getFirestore } from "firebase/firestore";
import { getDatabase } from "firebase/database";

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_BUCKET",
  messagingSenderId: "YOUR_MSG_ID",
  appId: "YOUR_APP_ID",
  databaseURL: "YOUR_DB_URL"
};

const app = initializeApp(firebaseConfig);
export const auth = getAuth(app);
export const firestore = getFirestore(app);
export const realtimeDB = getDatabase(app);
