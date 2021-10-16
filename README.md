# Assignment for Frontend Engineer job applicants

## Background

Your task is to implement a simple CRUD application. The application is based on [Conduit, "The mother of all demo apps"](https://github.com/gothinkster/realworld), which is a simple clone of [Medium.com](https://medium.com/). The demo of the application can be found at https://demo.realworld.io/.

You will find OpenAPI Specification (Swagger 2.0) for the API to use with this project in `docs/schema/swagger.json`. We recommend [Swagger Editor](https://editor.swagger.io/) to explore it in human readable format.

## Business requirements

The application, as the entry point, should display the articles list page. Since the assignment is time constrained, it would be impossible to fully implement the project. Please implement at most the pages mentioned in the next section. If you think we expect too much, please let us know what you have omitted and try to explain your reasoning.

### Pages

#### Homepage / Articles list

The articles list page should display the list of articles with:
* Article title
* Article description
* Date of publication
* Article author
* Button to favorite article (with favorite count)

Please ignore implementation of tags section, it is included for improved visuals of this page.

Link each article displayed to a dedicated page with the article content.

Link each author displayed to a dedicated page with the author profile content.

#### Article

The article page should display:
* Article title
* Article body
* Date of publication
* Article author
* Button to favorite article (with favorites count)
* Button to follow author (with followers count)
* _optional: Convert article body from Markdown text to HTML_

Please ignore implementation of comment section, it is included for improved visuals of this page.

#### Profile

The profile page should display:
* Author name
* Author bio
* Author image
* Button to follow author (with followers count)
* List of articles written by that author 

#### Login

The login page should display form with email and password. The user of the application should be able to log in using the following credentials:

| Email               | Password           |
|---------------------|--------------------|
| `alice@example.com` | `I_<3-R0ber7`      |
| `bob@example.com`   | `4L1ce-I5 mY_li3f` |

Please ignore implementation of user registration.

#### Logout

The logout must log the user out and redirect to homepage.

### Components

#### Author image

Use placeholder image if author image is not available.

#### Favorite article and Follow author buttons

The buttons should visually indicate whether the article is favorited or the author is followed by currently logged in user.

## Technical requirements

The solution should be implemented with React using provided [Create React App](https://create-react-app.dev/) skeleton. The skeleton does not have any structure on purpose, we have just provided you with all pages for the application with HTML taken from [Conduit templates](https://gothinkster.github.io/realworld/docs/specs/frontend-specs/templates).

You can use either JavaScript or TypeScript as your technical stack. Although we have decided to implement the skeleton in TypeScript, we have not implemented any types so you can use it as regular JavaScript.\
You can also use any open source dependencies you want, but be considerate – dependencies for network requests, routing, timedate manipulations and design systems should be sufficient.\
Please clone this repository on [Github](https://github.com/) using [Git](https://git-scm.com/) and make it public.

For your convenience, we have included the backend application providing the API as a Docker image which you can run together with database using [Docker Compose](https://docs.docker.com/compose/).

You can run the backend application by executing:

    docker-compose up

You will also need to initialise the database (first time you use it or any time you want to reset it to initial state), to do so run:

    docker-compose run --rm api npm run db:reset

After running the above commands, the API should be accessible on http://localhost:3000/.

To clean up the backend application completely and start over, run:

    docker-compose down --remove-orphans

The application you create should also run inside a [Docker](https://www.docker.com/) container, as it will greatly improve the ease of setup and testing when we review your solution. For your convenience we have provided a `Dockerfile` that should already work.

This is how we should be able to run the application:

    docker build -t job-assignment-frontend-engineer .
    docker run --rm -p 8080:80 job-assignment-frontend-engineer

Running the above in fresh clone of this repository should result in the skeleton application to be started and made accessible on http://localhost:8080/.

## Tips

The goal of this task is to provide a discussion context for the subsequent technical interview and is not meant to be time consuming.
Although it is intended for all levels of Frontend Developers, we expect more attention to detail the more experienced you are.

Using solutions recommended by React is preferred. 
You can emphasise on certain aspects of the task to showcase your skills, either through cleverly using React built in mechanisms or leaving `TODO` notes for more advanced solutions that come to your mind or when taking shortcuts to reduce development time.

The time to complete this project will depend on your expertise, but based on our own employees executing this task, we estimate that it should not take more than 4-8 hours depending on your proficiency.
We understand and honor that you have a life outside work so we recommend that you do not exceed the above mentioned limit.

Do not invest your time into implementing additional business requirements that are not listed and please leave the application design unchanged.

We would like to see one unit test (of different types of code) being showcased, but by any means please do not try ensuring 100% coverage – while it’s never a waste of time in real projects, we don’t want you to waste it for homework assignment.


## Evaluation criteria

There are certain aspects that will be considered when evaluating your solution:

* code quality
* implementation according to the specifications
* expertise in using React
* expertise in using external dependencies
* expertise in using git
* expertise in testing your own code
* expertise in working with HTML5 and Web APIs
* expertise in working with CSS
* expertise in calling external APIs


## Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

### Available Scripts

In the project directory, you can run:

#### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

#### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

#### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

#### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

### Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
