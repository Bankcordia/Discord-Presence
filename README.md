# Discord-Presence
This is a guide on how to have the brand new Rich-Presence beta on your profile!

> ## Setup the Rich Presence
> - Step One: Download [Node JS](https://nodejs.org/), please make sure to have the LTS version.
> - Step Two: Download [Visual Studio Code](https://code.visualstudio.com/)
> - Step Three: Open your command promt (You can do this by pressing `WINDOWS + R` on your keyboard, and then typing `cmd`.
> - Step Four: in your command promt, type `cd Desktop`. (This is going to cd in to your Desktop directory.)
> - Step Five: in your command promt, type `mkdir Rich-Presence`. (This is going to create a new folder in your Desktop called "Rich-Presence.)
> - Step Six:  in your command promt, type `npm init --y`. (This will create the node_modules folder, make the package.json and package-lock.json.)
> - Step Seven: In your command promt, type `npm i discord-rpc`. (This will download the module you NEED for this to work.)
> - Step Eight: In your command promt type `code .`. (This will open [Visual Studio Code](https://code.visualstudio.com) to the folder you have created.)
> - Step Nine: In Visual Studio Code, create a new file called `index.js`. (This will create a JavaScript file which allows us to edit JavaScript code.)
> - Step Ten: In Visual Studio Code, go to your file named `index.js`, and paste this code:
 ```js
const { Client } = require('discord-rpc');

const client = new Client({ transport: 'ipc' });

client.on('ready', () => {

  client.request('SET_ACTIVITY', {
    pid: process.pid,
    activity: {
      assets: {
        large_image: 'Your_Discord_Developer_Portal_Asset_ID',
      },
      buttons: [
        {label: 'Website', url: 'https://blurple.gg/'},
        {label: 'Discord Server', url: 'https://blurple.gg/discord'},
      ],
      
    }
    
  
})
console.log(client.user.username+"#"+client.user.discriminator+"\'s presence has updated (I Think)")
})

client.login({clientId: 'Your_Discord_Developer_portal_application_clientID'})```

*Please join [Blurple Development](https://blurple.gg/discord) if you are having issues with this presence guide.*
