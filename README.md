# OIT_code_challenge

Code Challenge for BYU OIT Software Developer Application

The files I created/edited are as follows: 

src/App.vue
src/webapp/Form.vue
src/webapp/Display.vue

During the 4 hours, I spent time studying Vue as I have never used this framework before. Additional time was spent with first time set up for the Vue framework.

After learning how Vue creates and uses components I created 2 components (both in webapp due to time constraints) that are called onto the main App.vue page.

In Form.vue, I originally created a form to capture user input. Later in my study I discovered that v-model is a shortcut way of capturing user input into a variable. This is why the file is named Form when no form element is used.

In Form.vue I verified the the input was being captured by having an element dynamically display the user's query. I was unable to verify the query correctly being sent to the API due to errors I did not have time to remedy.

In Display.vue, I planned on displaying the information of the queried movie. The component correctly gets imported into App.vue. I have also managed to correctly perform an API call sending a request and receiving a response for the movie "Fight Club" from themoviedb.org

Unfortunately, I have been unable to format the response. Every time I try to select certain elements of the JSON (such as "title"), my Vue project breaks prompting a hard refresh. I am only able to display the entire object. 

Finally, I apologize for any difficulty checking the this program. VS Code was having difficulty with Git so I had to manually upload my files. 
