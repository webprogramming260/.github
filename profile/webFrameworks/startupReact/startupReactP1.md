# Startup React Phase 1: HTML/CSS

Now that you understand what a web framework is and have practiced by converting Simon CSS into a React application, it is time to convert your application to use React. The process of converting code from one way of doing things to different way is called **porting**. Porting is a very common software engineering task and hopefully this deliverable will help you to start getting comfortable with the process.

Porting your application to React will require significant modifications to your frontend code. Make sure you reserve enough time to successfully complete this work.

⚠ This phase only converts your HTML and CSS over to React. You do not need to implement any interactivity into your application for this phase. That will come in the [second JavaScript phase](startupReactP2.md) of this deliverable.

You must use the same startup GitHub repository that you created in the earlier instruction. Update the `notes.md` file with things that you learn as you work on your startup. As you make changes to your application, commit those changes and push them to GitHub. Make sure you have enough commits that you can demonstrate your ownership of the code and protect yourself from loss. Usually this will mean at least ten commits, but in reality you may have many more than that. Failing to fully document your work may result in the rejection of your submission.

Remember to use the the browser's debugger window to debug your CSS and JavaScript. You will host your React application using Vite's hot reloading HTTP server.

Once you have fully ported the HTML/CSS version of your application over to use React, you need to release it to your production environment. **Replace** your previous startup deployment script with a copy of the `deployReact.sh` script from the [Simon React repository](https://github.com/webprogramming260/simon-react/blob/main/deployReact.sh) and use `startup` for the service parameter (`-s`).

```sh
./deployReact.sh -k <yourpemkey> -h <yourdomain> -s startup
```

For example,

```sh
./deployReact.sh -k ~/keys/production.pem -h yourdomain.click -s startup
```

Doing this will make this deliverable of your startup available from `https://startup.yourdomainname`.

## ☑ Assignment

1. Port Simon CSS to use React as defined in the [Simon React Part 1](../../simon/simonReact/simonReactP1.md) instruction.
   1. Clone the Simon CSS repository to your development environment.
   1. Follow all the instructions for porting Simon to [React](../../simon/simonReact/simonReactP1.md)
   1. Deploy your ported version of Simon CSS to your production environment copying and using the `deployReact.sh` deployment script from the [Simon React repository](https://github.com/webprogramming260/simon-react/blob/main/deployReact.sh).
1. Convert your HTML/CSS startup frontend to use React. This includes:
   1. Creating a template starting application using `vite` and cleaning up what it created.
   1. Creating a react router that displays stubbed components for the main pieces of your application.
   1. Converting your previous HTML files into the stubbed components with proper references to your CSS files.
1. Make sure your name is displayed in the application and that there is a link to your GitHub repository.
1. Periodically commit and push your code to GitHub.
1. Periodically update your startup repository's `notes.md` file to reflect what you have learned and want to remember.
1. Push your final version of your project to GitHub.
1. Deploy your startup application to your production environment (your server).
1. Make sure your application is available from your production environment.
1. Upload the URL to your startup application to the Canvas assignment.

## Grading Rubric

- **Prerequisite**: Ported version of Simon CSS ported to Simon React and deployed to your production environment
- **Prerequisite**: A link to your GitHub startup repository prominently displayed on your application's home page
- **Prerequisite**: Notes in your startup Git repository `README.md` file documenting what you modified and added with this deliverable. The TAs will only grade things that have been clearly described as being completed. Review the [voter app](https://github.com/webprogramming260/startup-example) as an example.
- **Prerequisite**: Enough Git commits to fully prove your ownership of your code. This usually means dozens of commits spread across multiple days of the deliverable development period. Failure to do this may result in the rejection of your submission.
- Application converted to use React
  - 10% Bundled using Vite
  - 50% Multiple react components that contain your HTML and CSS. No interactivity is required at this point.
  - 40% React router

## Go celebrate

With the port to React your startup should now feel like a modern web application. Time to celebrate. I'm thinking lollipops. 🍭