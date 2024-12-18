# Startup React Phase 2: JavaScript

With your startup ported to React it is time to implement all of the interactivity necessary to make your application functional. This includes writing significant JavaScript such that a user can fully interact with the application.

Making your application interactive will require significant modifications to your frontend code. Make sure you reserve enough time to successfully complete this work.

## Mocking out functionality

For parts of your application that require third party services, backend service support, or database persistence, you will need to stub, or mock, out those pieces in your JavaScript. Here are some examples of how you can stub out functionality.

1. **Local storage**: If you need to store credentials or game state you can use the browser's [localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) until you have a database where you can store such information. Note that this data will only be available on the browser where the data was created.
   ```js
   localStorage.setItem('userName', 'Tom');
   const userName = localStorage.getItem('userName');
   ```
1. **Hard coded responses**: If you need an endpoint that provides external data such as a weather report or a LLM response you can simply hard code a single response that looks exactly like what a future endpoint will return.
   ```js
   function getWeather() {
     return { date: '2026-05-20', outlook: 'fair' };
   }
   const weather = getWeather();
   ```
1. **setInterval**: If you need data that would have be pushed from a server over a WebSocket for functionality such as a stock price update or a peer chat message, you can use the `setInterval` function.
   ```js
   setInterval(() => console.log('event'), 1000);
   ```

## Getting started

You must use the same startup GitHub repository that you created in the earlier instruction. Update the `notes.md` file with things that you learn as you work on your startup. As you make changes to your application, commit those changes and push them to GitHub. Make sure you have enough commits that you can demonstrate your ownership of the code and protect yourself from loss. Usually this will mean at least ten commits, but in reality you may have many more than that. Failing to fully document your work may result in the rejection of your submission.

Remember to use the the browser's debugger window to debug your CSS and JavaScript. You can also debug your service JavaScript running on Node.js using the built in VS Code Node.js debugger.

Once you have developed your application to where you want it, you need to release it to your production environment. Use the same `deployReact.sh` script that you used in the previous React deliverable. Make sure to use `startup` for the service parameter (`-s`).

```sh
./deployReact.sh -k <yourpemkey> -h <yourdomain> -s startup
```

For example,

```sh
./deployReact.sh -k ~/keys/production.pem -h yourdomain.click -s startup
```

Doing this will make this deliverable of your startup available from `https://startup.yourdomainname`.

## ☑ Assignment

1. Review and deploy Simon React
   1. Clone the Simon React repository to your development environment.
   1. Execute your frontend code in your development environment by running `npm run dev` from the console in the root of the project. This will automatically open your browser to https://localhost:5173. Use the browser's dev tools to step through the frontend JavaScript using the Source tab.
   1. Deploy to your production environment using the deployment script so that it is available with your domain's `simon` subdomain.
1. Convert your startup frontend to use React. This includes:
   1. Creating a template starting application using `vite` and cleaning up what it created.
   1. Creating a react router that displays stubbed components for the main pieces of your application.
   1. Converting your previous HTML files into the stubbed components.
1. Make sure your name is displayed in the application and that there is a link to your GitHub repository.
1. Periodically commit and push your code to GitHub.
1. Periodically update your startup repository's `notes.md` file to reflect what you have learned and want to remember.
1. Push your final version of your project to GitHub.
1. Deploy your startup application to your production environment (your server).
1. Make sure your application is available from your production environment.
1. Upload the URL to your startup application to the Canvas assignment.

## Grading Rubric

- **Prerequisite**: Simon React deployed to your production environment
- **Prerequisite**: A link to your GitHub startup repository prominently displayed on your application's home page
- **Prerequisite**: Notes in your startup Git repository `README.md` file documenting what you modified and added with this deliverable. The TAs will only grade things that have been clearly described as being completed. Review the [voter app](https://github.com/webprogramming260/startup-example) as an example.
- **Prerequisite**: Enough Git commits to fully prove your ownership of your code. This usually means dozens of commits spread across multiple days of the deliverable development period. Failure to do this may result in the rejection of your submission.
- Application converted to use React
  - 70% Multiple react components that implement or mock all app functionality
  - 30% React `useState` and `useEffect` hooks

## Go celebrate

With the addition of interactivity to your startup it should be basically functional. Anything that remains should be stubbed out in some way that makes the application usable. Time to celebrate. I'm thinking tacos. 🌮