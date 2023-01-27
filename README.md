# Birthday Wrapped

![photos](https://github.com/dariusz-grubba/BirthdayWrapped/blob/903423adfbae30418ea32b4c046ddee9efe319f1/src/phone.png)

<!-- ### Features

- Displaying the current time and date;
- Countdown to the next break;
- Passing the next lesson from the timetable;
- Informing about the end of the lesson;
- Countdown to the next school break (e.g., spring break) -->

# [Preview link](https://birthday-wrapped-project.vercel.app/ "Preview link")

<!-- Add the PWA’s icon to a home screen

- iOS

1. Open the browser by tapping on the Safari icon.
2. Navigate to the PWA url.
3. Tap on the Share button at the bottom of the browser window. It's represented by a square with an up arrow in the foreground.
4. The iOS Share Sheet will now appear, overlaying the main browser window. Select the option labeled "Add to home screen".

- Android

1. Open Chrome Chrome.
2. Navigate to the PWA url.
3. Tap Install.
4. Follow the on-screen instructions. -->


# About

The project was created using the [zuck.js](https://github.com/ramonszo/zuck.js "zuck.js") library. This made it possible to create Instagram-like stories.




# Uploading your own stories



Initialize:

```js
let stories = new Zuck(`{{element id string or element reference}}`, {
  skin: 'snapgram',      // container class
  avatars: true,         // shows user photo instead of last story item preview
  list: false,           // displays a timeline instead of carousel
  openEffect: true,      // enables effect when opening story
  cubeEffect: false,     // enables the 3d cube effect when sliding story
  autoFullScreen: false, // enables fullscreen on mobile browsers
  backButton: true,      // adds a back button to close the story viewer
  backNative: false,     // uses window history to enable back button on browsers/android
  previousTap: true,     // use 1/3 of the screen to navigate to previous item when tap the story
  localStorage: true,    // set true to save "seen" position. Element must have a id to save properly.
  reactive: true,        // set true if you use frameworks like React to control the timeline (see react.sample.html)
  rtl: false,            // enable/disable RTL

  stories: [ // array of stories
    // see stories structure example
  ],

  callbacks:  {
    onOpen (storyId, callback) {
      callback();  // on open story viewer
    },

    onView (storyId) {
      // on view story
    },

    onEnd (storyId, callback) {
      callback();  // on end story
    },

    onClose (storyId, callback) {
      callback();  // on close story viewer
    },

    onNavigateItem (storyId, nextStoryId, callback) {
      callback();  // on navigate item of story
    },

    onDataUpdate (currentState, callback) {
      callback(); // use to update state on your reactive framework
    }
  },

  template: {
    // use these functions to render custom templates
    // see src/zuck.js for more details

    timelineItem (itemData) {
      return ``;
    },

    timelineStoryItem (itemData) {
      return ``;
    },

    viewerItem (storyData, currentStoryItem) {
      return ``;
    },

    viewerItemPointer (index, currentIndex, item) {
      return ``;
    },

    viewerItemBody (index, currentIndex, item) {
      return ``;
    }
  },

  language: { // if you need to translate :)
    unmute: 'Touch to unmute',
    keyboardTip: 'Press space to see next',
    visitLink: 'Visit link',
    time: {
      ago:'ago', 
      hour:'hour', 
      hours:'hours', 
      minute:'minute', 
      minutes:'minutes', 
      fromnow: 'from now', 
      seconds:'seconds', 
      yesterday: 'yesterday', 
      tomorrow: 'tomorrow', 
      days:'days'
    }
  }
});
```

Add/update a story (timeline item):

```js   
stories.update({item object});
 ```

Remove a story:

```js
stories.remove(storyId); // story id
```

Add/remove a story item:

```js
stories.addItem(storyId, {item object});
stories.removeItem(storyId, itemId);
```



<!-- # Installation

To install **MyClock** and run it on localhost , install **Node.js** and use the following commands in the terminal:

`$ npm install`

Opens the application in developer mode.
[http://localhost:3000](http://localhost:3000) Opens on the local server in the browser.

`$  npm start`

Launches test mode in interactive observation mode.

`$  npm test`

Builds the application for production in the `build` folder.

`$  npm run build`

You can find more information about it here: [https://facebook.github.io/create-react-app/docs/deploymen](https://facebook.github.io/create-react-app/docs/deployment) -->