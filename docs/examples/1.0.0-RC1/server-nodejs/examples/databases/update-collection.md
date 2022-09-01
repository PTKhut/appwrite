const sdk = require('node-appwrite');

// Init SDK
const client = new sdk.Client();

const databases = new sdk.Databases(client);

client
    .setEndpoint('https://[HOSTNAME_OR_IP]/v1') // Your API Endpoint
    .setProject('5df5acd0d48c2') // Your project ID
    .setKey('919c2d18fb5d4...a2ae413da83346ad2') // Your secret API key
;

const promise = databases.updateCollection('[DATABASE_ID]', '[COLLECTION_ID]', '[NAME]', false);

promise.then(function (response) {
    console.log(response);
}, function (error) {
    console.log(error);
});