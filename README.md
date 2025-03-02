# Personal Website

This project is a simple, but carefully structured web application that serves as personal portfolio and landing page. It demonstrates how to integrate modern technologies (Nuxt 3, Vue 3 with TypeScript and Tailwind CSS) to create a responsive and elegant interface with visual effects such as glass effect (glassmorphism), smooth transitions and blur filters. Access here: https://fiap-personal-site.vercel.app

---

## Sumary

- [Personal Website](#personal-website)
  - [Sumary](#sumary)
  - [Description](#description)
  - [Features](#features)
  - [Technologies](#technologies)
  - [Installation and Configuration](#installation-and-configuration)
    - [Prerequisites](#prerequisites)
    - [Steps](#steps)
  - [Execution of the project](#execution-of-the-project)
  - [Build \& Deploy](#build--deploy)
    - [Deploy](#deploy)
  - [Customizations](#customizations)
  - [License](#license)
  - [Final Considerations](#final-considerations)

---

## Description

This personal website was developed to serve as a portfolio and digital business card. Although the application is simple, it has been built with the best practices of software engineering, using:

- Nuxt 3 for server-side and client-side structuring and rendering;
- Vue 3 with TypeScript to ensure static typing and more robust code;
- Tailwind CSS for fast and responsive styling, plus modern customizations like glass effect and smooth transitions;
- Responsiveness and Mobile First: Responsive menu with mobile sidebar, modal transitions and smooth scroll.

> The project demonstrates not only development skills, but also attention to design details and user experience.

---

## Features

- **Header with Glass Effect**: A fixed header with semi-transparent and blurred background (glassmorphism) that adapts to all resolutions.
- **Responsive menu**: Desktop and mobile navigation with hamburger button that opens a sidebar.
- **Hero section**: Highlight area with background image, overlay, sophisticated positioning of texts and profile picture.
- **Modal with Transition**: Display additional information (Fun Fact or About Me) with fade effect using the `<transition>` component.
- **Smooth Scroll**: Implemented globally via CSS for fluid navigation between sections of the page.
- **Filters and Text Shading**: Use custom utilities in Tailwind for advanced visual effects, such as text-shadow and backdrop blur.

---

## Technologies

- **Nuxt 3**: Framework for Vue.js that facilitates the creation of universal applications (SSR + SPA).
- **Vue 3**: Progressive library for building interfaces.
- **TypeScript**: Superset of JavaScript that adds static typing.
- **Tailwind CSS**: Utility-first framework for responsive and customizable design.
- **PostCSS**: CSS processor used in conjunction with Tailwind to transform and optimize styles.

---

## Installation and Configuration

### Prerequisites

Node.js (version 14 or higher)
npm or Yarn

### Steps

1. Clone the repository:

```
git clone https://github.com/matheusarjc/Fiap-PersonalSite.git
cd Fiap-PersonalSite
```

2. Instale as dependências:

```

npm install
/or
yarn install
```

3. Nuxt and Tailwind configuration:

**Nuxt 3** is already configured to use TypeScript. The official Tailwind CSS module is installed and configured in the nuxt.config.ts file, where the Google Fonts font is also imported:

```
// nuxt.config.ts
export default defineNuxtConfig({
  modules: ['@nuxtjs/tailwindcss'],
  app: {
    head: {
      link: [
        { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;...&display=swap' }
      ]
    }
  },
  // Nuxt configs
})
```

> The tailwind.config.js file has been configured to include the directories where Tailwind should fetch classes:

```

/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    './app.vue',
    './components/**/*.{vue,js,ts}',
    './pages/**/*.{vue,js,ts}',
    './plugins/**/*.{vue,js,ts}'
  ],
  theme: {
    extend: {
      fontFamily: {
        poppins: ['Poppins', 'sans-serif'],
      },
      // Others extensions
    },
  },
  plugins: [],
}
```

4. Arquivo de Estilos Global:

In the file `assets/css/main.css`, you have the directives:

```
@import "tailwindcss";

@layer utilities {
  .text-shadow-custom {
    text-shadow: 0 3px 2px rgba(0, 0, 0, 0.6);
  }
  .text-shadow-custom-blur {
    text-shadow: 0px 3px 6px rgba(0, 0, 0, 0.6);
  }

  .shadow-img {
    box-shadow: 0px 10px 16px -1px rgba(0, 0, 0, 0.75);
    -webkit-box-shadow: 0px 10px 16px -1px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: 0px 10px 16px -1px rgba(0, 0, 0, 0.75);
  }

  .bg-template {
    background-color: #0b0b0b;
  }
}
```

In addiction, in the file `assets/css/global.css` you have:

```

@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Tenor+Sans&display=swap");

html {
  scroll-behavior: smooth;
}

body {
  font-family: "Poppins", sans-serif;
}
```

---

## Execution of the project

To run the project in development mode, perform:

```
npm run dev
```

Access http://localhost:3000 in your browser. You will be able to view the site with all features, including the glass-effect header, responsive menu and modal transitions. Otherwise, you can access at https://fiap-personal-site.vercel.app

## Build & Deploy

To create an optimized production version:

```
npm run build
```

The /.output directory (or dist, depending on configuration) will be generated. To run the production version locally:

```
npm run preview
```

### Deploy

**Nuxt 3** is compatible with several deployment platforms, such as:

- Vercel
- Netlify
- Heroku
- Docker

> Configure the deploy according to the documentation of the chosen platform. It is recommended to integrate with GitHub for continuous deployment.

## Customizations

- **Layout and Themes**:
  You can change the theme directly in tailwind.config.js to adjust colors, fonts and spacing according to your visual identity.

- **Components**:
  Each section of the site (Header, Hero, Modal, About, Projects, Contact) is modularized in Vue components. This facilitates maintenance and future expansions.

- **Effects and Transitions**:
  We use the transition classes of Tailwind to smooth the modal display. You can experiment with other classes or customize the values as needed.

- **Integration with APIs**:
  Even though it is a simple application, the code has been structured in order to allow future integrations with APIs, if necessary.

## License

This project is licensed under the MIT License.

## Final Considerations

This repository serves not only as a personal portfolio, but also as an example of good development practices, even for simple applications. In addiction, **IT ISN´T MY PORTFOLIO, ITS JUST AN EXAMPLE!** The modular structure, use of TypeScript and integration with modern tools ensure that code is easy to maintain and expand by following the standards of a software engineer.

If you have questions or suggestions, feel free to open an issue or send a pull request. I am always looking to improve and learn from the community!
