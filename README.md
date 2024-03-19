# ORwy2bZ9yOOjY5g-
API for Deriv.VRTC.demo.auto.
npm install ws 
yarn add ws 
const WebSocket = require('ws');
const DerivAPI = require('@deriv/deriv-api/dist/DerivAPI');

// app_id 1089 is for testing, create your own app_id and use it here.
// go to api.deriv.com to register your own app.
const connection = new WebSocket('wss://ws.derivws.com/websockets/v3?app_id=1089');
const api        = new DerivAPI({ connection });
const basic = api.basic;

basic.ping().then(console.log);
