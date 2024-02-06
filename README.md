# Improving Frontend Development with Storybook
By [Divyanshu Garg](https://medium.com/@divyanshugarg36)
![Storybook](https://miro.medium.com/v2/resize:fit:828/format:webp/1*NP0sTtoAxuijP1e8wIitbw.png)
<p align="center">Storybook<p>


## Introduction

After developing WebApps for almost five years, I always wondered every time what could be done to manage the front-end application better. Based on the principle of atomicity, a simple approach of preparing a UI kit of the application and then consuming the same components to build every feature of the App.

Recently, I got introduced to something new and exciting (at least for me). One of my co-developers suggested using Storybook.

*[Storybook](https://storybook.js.org/) is a frontend workshop for building UI components and pages in isolation. Thousands of teams use it for UI development, testing, and documentation. It’s open source and free.*

## Solutions?
Why do we need a Storybook?

To know the why, we need to understand the problems first. Working on a large frontend project can be painful when the developers have to deal with n number of features and add a cherry on the top n+n number of components that are necessarily required to build a clean and bug-free application. But, dealing with n number of components and memorising all of them won’t be easy for everyone, that is where the storybook comes to the rescue.

-   **Maintaining the principle of** [**Atomicity**](https://docs.spryker.com/docs/scos/dev/front-end-development/202311.0/yves/atomic-frontend/atomic-front-end-general-overview.html#component-model)  — Believe it or not, in my experience maintaining atomic development patterns saves a lot of time. Using Storybook forces the developer to focus on the root functionality of the target component and ensures that no application logic is involved. But to get there, developing the component in the isolated Storybook environment is important.

-   **Easy documentation**  — Documentation is an important part of the development process. Storybook allows us to create  [MDX2](https://mdxjs.com/blog/v2/)-based document files that are converted to beautiful-looking documentation with user-interactive features that can be easily added. Moreover, By using docstrings, Storybook will automatically process those comments to display the information in the form of UI.

![MDX2 Documentation](https://miro.medium.com/v2/resize:fit:839/1*eK62qmcTO7ACHVA01edk0w.png)
<p align="center">MDX2 Documentation</p>

-   **Scalability and Source—**  This depends upon the extent of the project a developer is working on and is mostly based on my current use case. I am working on a chain of multiple projects that use the same components in every project as all the projects lie under the same product. Duplicating the components for each project doesn't sound like an appropriate option. Additionally, in the short term, it won’t affect the code a lot but in the long term, there is a huge possibility that the result is different versions of the same components spread across different repositories.  
    Thus treating those components as a separate package integrated with Storybook can allow us to create an environment that can be easily upgraded and extended, also acting as a single source of truth and trust to ensure that updates and fixes pushed on a single place can change it in all the applications.
    
-   **Team sharing —**  Ever been in a situation where the dev ended up sharing the same information with multiple teammates, multiple times? Well, the Storybook helps in doing that in just a single go. By deploying the storybook, anyone can access the documentation and go through every piece of information that has been put together.

-   **Testing —**  From allowing devs to generate beautiful documentation to testing, Storybook comes with a huge range of test coverage starting from Spot testing all the way along to Visual test appearance, Interaction test, Accessibility test, and Snapshot test markup. Additionally, QA can be easily performed using the interface provided by Storybook.

![Storybook Tests](https://miro.medium.com/v2/resize:fit:839/1*eBk8hfa8w3aFNH3acr5_Lw.png)<p align="center">Storybook Tests</p>

## [Setup](https://storybook.js.org/docs/get-started/install)  (Next.JS)

1.  Setup Next.JS (Choice of framework)
2.  Run the following command:-

   *`npx storybook@latest init`*

![Storybook setup](https://miro.medium.com/v2/resize:fit:839/1*UWxEEV5uEB3fr4yZXZuicg.png)
<p align="center">Storybook setup</p>

3. That is it, it will automatically setup the project and run the server.
![Storybook (Fisrt initialization)](https://miro.medium.com/v2/resize:fit:839/1*kk7gntNQyzTXMRwy3GoWDA.png)
<p align="center">Storybook (Fisrt initialization)</p>

4. You will find several examples to get the project started.

## Conclusion

Since the use case for Storybook can vary based on the requirements and scope of the project, integrating Storybook in small projects might not be beneficial, but on the other side in large projects, it can save lives. The extent of benefits depends on how the storybook is setup in the project. Maintaining additional code costs time and money, but you are the one to decide if investing that time in managing the storybook code is worth it for the project or not.

Keep Coding!!
