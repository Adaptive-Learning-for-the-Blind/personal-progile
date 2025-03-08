# Building an Accessible Web Profile: Part 1 - Building the Page

## Introduction

There's something special about building your very first website—a digital space that truly belongs to you. In this beginner-friendly tutorial, we'll create a personal profile page where you can share your information and, eventually, showcase your projects as your skills grow. No matter where you are on your coding journey, having your own web presence is an empowering first step!

In this series, we'll build a modern profile page featuring your name, contact details, and social media links—all designed to be fully accessible. We'll even add a dark/light theme toggle to enhance usability for everyone. Best of all, our design will fit on a single screen, making navigation effortless.

By building this project step-by-step, you'll discover exactly what makes a website accessible. You'll learn the specific structures, attributes, and techniques that create a seamless experience for screen reader users. Since you already navigate the web with a screen reader, you'll gain a deeper understanding of how the code you write translates to the experience you encounter daily.

We've divided this project into three manageable articles:

1. **Part 1: Building the Page - You are here!** We'll set up our development environment and create the structure of our page.
2. **Part 2: Adding Theme Toggle Functionality:** We'll add code to make the theme toggle button switch between light and dark modes.
3. **Part 3: Deployment**  We'll publish your page to the web so others can see it.

Let's get started with setting up our tools!

## Tools and Set Up 

Before we start building our page, we need to install a code editor. A code editor is a specialized text editor designed for writing code. While you might be familiar with word processors like Microsoft Word for writing documents, these programs won't work for coding. Word processors add invisible formatting characters and tend to automatically "correct" things like quotes and indentation that are crucial for code to function properly.

A proper code editor provides helpful features like auto-completion, and error checking that make writing code much easier. Many even offer specialized tools for web development and accessibility.

Visual Studio Code (or VS Code) is a popular, free code editor created by Microsoft that works well across all operating systems. It's highly customizable, has excellent support for web development, and includes built-in features to work with screen readers. 
### Visual Studio Code Installation Guide

1. Visit the [Visual Studio Code website](https://code.visualstudio.com/)
2. Click the download button for your operating system (Windows, Mac, or Linux) 
3. Run the installer after it downloads 
4. During installation, make sure to select these important options:
	- For Windows users: Check "Add to PATH" so you can open VS Code from the command prompt
	- Check "Add 'Open with Code' action to Windows Explorer file context menu" 
	- Check "Add 'Open with Code' action to Windows Explorer directory context menu" 
	- Check "Add to System Path"
5. Once installed, launch VS Code

### Visual Studio Code Basic Navigation for Beginners
VS Code has excellent screen reader support, but you'll need to ensure that screen reader mode is activated for the best experience.

When you first open VS Code with a screen reader running, it should automatically detect your screen reader and ask you if you'd liek to enable screen reader mode. If this doesn't happen:

1. Press `Ctrl+,` (Windows/Linux) or `Cmd+,` (Mac) to open Settings
2. Type "screen reader" in the search box
3. Find the "Editor: Accessibility Support" setting
4. Change it to "on"
5. Press `CTRL+w`to close the setting window
### Understanding VS Code's Layout
VS Code follows a familiar Microsoft application layout that you may recognize. Since it's developed by Microsoft, many of the keyboard shortcuts and navigation patterns you've used in other Microsoft products will work here too.

The interface consists of:
- **Activity Bar**: Located on the far left, it contains icons for different views
- **Side Bar**: Next to the Activity Bar, shows context-specific information like files or search results
- **Editor Area**: The main area where you'll write code
- **Status Bar**: At the bottom, displays information about your project, similar to status bars in other Microsoft applications

If you've used applications like Microsoft Word or Outlook, you'll notice the same attention to keyboard accessibility and similar shortcut patterns in VS Code. For example, Ctrl+S to save, Ctrl+F to find, and Ctrl+N to create new files all work as expected.

Let's add a smooth transition from the previous section to connect the content better:

Now that we've gotten familiar with VS Code's layout and basic navigation, let's enhance our development environment by installing our first extension. Extensions allow us to customize VS Code with additional features, and the Live Server extension will be an essential tool for our web development work.

The Live Server extension simulates a web server on your computer, allowing you to view your web pages in a browser as if they were being hosted on the internet. When you're building a website, there's a difference between simply opening a file from your computer versus viewing it through a proper web address. Live Server creates a temporary web address on your computer (something like `http://localhost:3000`) that better represents how your page will function when published online.

To insall the Live Server Extension

1. Open VS Code
2. Press `Ctrl+Shift+X` to open the Extensions view
3. In the search box, type "Live Server"
4. Find "Live Server" by Ritwick Dey in the results (it should be the first result and have millions of downloads)
5. Press Tab to navigate to the Install button and press Enter
6. Wait for the installation to complete (VS Code will display a notification when done)

You can explore the VS Code Marketplace for other extensions that might enhance your development experience. In a future article, we'll provide a comprehensive guide to recommended extensions.
## Web Development Basics

With your development environment ready and Live Server installed, let's shift our focus to understanding the fundamental building blocks of web development. Before we start coding our profile page, it's important to understand the three core technologies that power the web.
### What is HTML? A Simple Explanation

HTML (HyperText Markup Language) is the foundation of every web page you encounter. Think of HTML as the structure or skeleton of a webpage. It defines the elements that make up your page and their organization.

HTML uses "tags" to define different types of content. Tags are enclosed in angle brackets, like `<this>`. Most HTML elements have an opening tag and a closing tag (with a forward slash), and your content goes between them.

For example, to create a heading, you would write:
```HTML
<h1>Your Name</h1>
```
The `<h1>` is an opening tag that says "this is a heading level 1," and the `</h1>` is a closing tag that indicates the end of the heading. "Your Name" is the content that will appear on the page.

Well-structured HTML is crucial for accessibility. The browser interprets your HTML code and creates what's called the accessibility tree - a simplified version of the page structure that screen readers can access. When you use proper HTML elements like headings, lists, and landmarks, the browser can provide this structural information to screen readers, allowing users to jump between sections, understand content hierarchy, and interact with the page more effectively. As you create web content, you'll experience firsthand how your code choices directly impact your navigation experience with a screen reader.
### What is CSS? Understanding Styling

CSS (Cascading Style Sheets) controls how HTML elements look and are positioned on the page. If HTML is the skeleton of a webpage, CSS is its appearance—the clothes, colors, and presentation. With CSS, you can control everything about the way an element looks on the page includeing the text size and color, padding and margin, and obrders.

In our project, we'll use Bootstrap, which is a collection of pre-written CSS (along with some JavaScript) that makes it easier to create attractive, consistent, and responsive websites.
### What is JavaScript? Adding Interactivity

JavaScript brings webpages to life by adding behavior and interactivity. While HTML provides structure and CSS handles appearance, JavaScript allows your page to respond to user actions.

In our profile page project, we'll use JavaScript to implement the dark/light theme toggle functionality, enhancing user experience while maintaining accessibility.

I understand! Let's focus on the "Project Set Up" section specifically, without code blocks. Here's the content for that section of your tutorial:

## Project Set Up
With our tools installed and a basic understanding of web technologies, we're ready to begin building our  profile page. Let's set up our project files and create the foundation for our website.

First, create a new folder on your computer named "my-profile-page" to keep all your project files organized. Then open VS Code and use Ctrl+O to open this folder as your project workspace. You can also open the folder form the File Explorer using the context menu options we set up earlier.

Now, let's create our main HTML file:

1. Press Ctrl+N to create a new file
2. Save it as "index.html" using Ctrl+S
3. Type `!` and press Tab to generate the HTML boilerplate

The boilerplate gives us a starting structure that every HTML page needs. We'll explore the HTML structure in detail in a future article, but for now, this gives us the foundation to start building.
### Adding a Page Title and Your First Heading

Now that we have our basic HTML file, let's customize it to make it truly yours. We'll start by adding your page title and your first heading.

The page title appears in the browser tab and in Google Search Results Page. it

1. Look for the `<title>` tag in the `<head>` section of your HTML file
2. It should look like: `<title>Document</title>`
3. Replace "Document" with your name and job/title.  
    ```
    <title>Your Name - Job Title</title>
	```
4. For example: `<title>Maria Johnson - Web Developer</title>`

Next, let's add a main heading to your page:

1. Find the `<body>` section of your HTML file
2. Move your cursor to the empty line between the opening body tat `<body>` and the closing body tag `</body>`
3. Create an `<h1>` heading with your name:    
    ```HTML
    <h1>Your Name</h1>
	```
4. For example: `<h1>Maria Johnson</h1>`

The `<h1>` tag represents the most important heading on the page. Screen readers announce this heading with special emphasis, helping users understand what the page is about right away.

Now let's see how your page looks in a browser:

1. Make sure your file is saved (press Ctrl+S)
2. Navigate to the status bar and select "Go Live
3. Alternatively, you can open your context menu from anywhere in VS Code and select "Open with Live Server"
4. A new browser window should open automatically showing your page
5. You should see your name displayed as a "heading level 1"

Live Server is especially helpful because it automatically refreshes your browser whenever you save changes to your files, allowing you to see updates immediately. Keep this window open while you're workng on the project.

If you're not seeing the changes you've made, make sure to save your file (Ctrl+S) and refresh your browser. You can also try restarting live server. 

1. Navgate to the status bar and selct "Port :550" (number may varry). this option replaces "Go Live" while Live Server is running.
2. When the "Go Live" optin appears again, you can selct it to restart the server.
## Introduction to Bootstrap

Once you've got your page working with a simple heading, it's time to enhance it with Bootstrap. Bootstrap is a free CSS framework that helps you build websites more easily. Think of it as a collection of pre-written styles and interactive components that you can apply to your HTML elements. This means you don't have to write complicated CSS yourself—Bootstrap has already done much of the work for you!

To use Bootstrap in our profile page, we'll add it using CDN (Content Delivery Network) links. This method is simple and doesn't require downloading files to your computer.

1. Within your HTML file, locate the `<head>` section
2. Just before the closing `</head>` tag, add the Bootstrap CSS link:
    ```HTML
	<link href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css" rel="stylesheet">
	```
3. Just below the `link` tag, add the Bootstrap JavaScript link:    
    ```HTML
	<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
	```

To verify that Bootstrap has been correctly added to your project, we can use the browser's developer tools.

1. Save your file (press Ctrl+S)
2. View your page using Live Server
3. Press F12 to open the browser's developer tools
4. Navigate to the element inspector where you can see all the HTML elements on the page.
5. Press Ctrl+F and type "bootstrap" to search for bootstrap references
6. Ffind references to `bootstrap.min.css` and `bootstrap.bundle.min.js` 
7. Navigate to the Console tab in the developer tools. This tab should be empty and have no errors.

The developer tools are a powerful way to examine and debug web pages. You can use them to explore the HTML structure of any website—try visiting your favorite sites and pressing F12 to learn how they're built!

When you're done checking, press F12 again to close the developer tools.
## Building the Page Structure

Now that we have Bootstrap set up, we'll begin constructing our profile page. Let's start by creating a basic structure with three main sections: header, main content, and footer. This layout will help organize our information in a clear, accessible way.

When building websites, it's important to use semantic HTML elements like `<header>`, `<main>`, and `<footer>` because they give meaning to the structure of your page—they tell browsers what each section is used for. This is especially important for screen reader users, as semantic elements create landmarks that make it easier to navigate through the page. When a screen reader encounters a `<header>` element, for example, it will announce "header" or "banner," allowing users to quickly understand and navigate the page structure.

Before we begin, we need to clear any content from between your `<body>` tags. If you've been following along, you'll have an `h1` heading there. Remove anything between the opening `<body>` and closing `</body>` tags, so you're starting with empty body tags like this:

```HTML
<body>
</body>
```

Next, modify your `<body>` tag to use Bootstrap's full-height classes:

```HTML
<body class="min-vh-100 d-flex flex-column">
```

These classes ensure that our page takes up at least the full height of the browser window and arranges our content in a vertical column.

Now, let's add our three sections:

```HTML
<header class="container py-4">
</header>
<main class="container flex-grow-1 d-flex align-items-center">
</main> 
<footer class="container py-3">
```

The `container` class creates a centered section with margins, while `flex-grow-1` on the main section makes it expand to fill available space between the header and footer.

Save your file (press Ctrl+S) and check your progress using Live Server. You won't see anything on the page, but you can use the Elements tab in the Developer Tools (F12) to verify that your `<head>`, `<main>` and `<footer>` tags are present.
## Building the Header Section

Before we add content to our header, let's talk about Bootstrap's grid system. Bootstrap provides a powerful layout tool that divides the screen into 12 equal columns. This grid system helps organize content in rows and columns, making it responsive across different screen sizes.

The basic structure uses three key components:

- `container` - Holds all your content with proper margins
- `row` - Creates horizontal groups of columns
- `col` - Defines the width of your content within the row

Using this system, we can position elements side-by-side and control how they align, which is perfect for our header where we'll have name and title on the left and a button on the right.

Let's structure our header with Bootstrap's row and column system:

1. Navigate to the empty header section in your HTML file (between the `<header>` and `</header>` tags)
2. Add the following code:
```HTML
<div class="row align-items-center">
	<div class="col">
		<h1>Your Name</h1>
		<p>Your Title</p>
	</div>
	<div class="col-auto">
	</div>
</div>
```

Now, personalize the header by replacing "Your Name" and "Your Title" with your information:

In addition to semantic tags and proper heading structure, here are some new accessibility features we've added with the above code.

1. **Descriptive IDs**: The `id` attributes (`profile-name`, `profile-title`) provide hooks for potential JavaScript interaction and make it easier to reference these elements.
2. **ARIA Label**: The `aria-label="Toggle dark or light theme"` on the button provides clear context to screen reader users about the button's function, which is especially helpful when the button state changes between dark and light modes.

Save your file and check your progress. Tab through the header elements to confirm your name is announced as a heading level 1, your professional title is read correctly, and the theme toggle button is announced with its aria-label "Toggle dark or light theme."
## Creating the Main Content Area

The main section of our profile page will contain your contact information, organized in a clean, accessible card layout. This is where visitors can find your email address and social media links.

## Setting Up the Main Content Section

We've already created the basic structure for our main section with the `<main>` tag and Bootstrap classes. Now let's add content to it. We'll use Bootstrap's card component. Cards are a flexible container for grouping related pieces of information together. They've' become a popular design pattern in modern web development because they create visual separation between different content sections, making information easier for sighted visitors to scan and understand. For our profile page, a card will help our contact information stand out.

1. Add a row and column structure to center our content:
```HTML
<div class="row">
	<div class="col-md-8 mx-auto">
	</div> 
</div>
```
2. Add a Bootstrap card component inside the column:
```HTML
<div class="card shadow">
	<div class="card-body">
		<h2 class="card-title mb-4" tabindex="0">Contact Information</h2>
	</div> 
</div>
```
3. Add the email section below the h2, but inside the `<div>` with class `card-body`:
```HTML
<div class="mb-3">
	<h3 class="h5" tabindex="0">Email</h3>
	<a href="mailto:alex@example.com" class="d-block mb-2" tabindex="0">        
		alex@example.com
	</a>
</div>
```
4. Add the social media links section above the closing div with the `card-body` class:
```HTML
<div class="mb-3">
	<h3 class="h5" tabindex="0">Social Media</h3>
	<ul class="list-unstyled">
		<li class="mb-2">
			<a href="https://twitter.com/alexjohnson" class="text-decoration-none">          
				Twitter: @alexjohnson
			</a>
		</li>
		<li class="mb-2">
			<a href="https://github.com/alexjohnson" class="text-decoration-none">           
				GitHub: alexjohnson
			</a>
		</li>
		<li>
			<a href="https://linkedin.com/in/alexjohnson" class="text-decoration-none">      
				LinkedIn: alexjohnson
			</a>
		</li>
	</ul>
</div>
```
5. Customize these sections with your own information:

Save your file with Ctrl+S and check your progress using your screen reader. Navigate through the main content to verify that headings and links are announced properly, ensuring that screen reader users can easily navigate your contact information.
## Building the Footer

The footer is the bottom section of your page and typically contains copyright information or other secondary details. Though simple, it's important to make the footer accessible and properly structured.

Add the following code inside the `<footer>` and `</footer>` tags.
```HTML
<div class="row">
	<div class="col text-center">
		<p tabindex="0">&copy; 2025 Alex Johnson. All rights reserved.</p>
	</div>
</div>
```
This code creates a centered paragraph with a copyright notice. The `&copy;` adds teh copright symbol. Remember to replace "Alex Johnson" with your own name.

Now that we've built all three main sections (header, main content, and footer), save your file and take a moment to review your completed page in the browser. Navigate through the page to verify that:
1. You can tab through all interactive elements like links and buttons
2. Headings are properly announced with their correct levels
3. The structure flows logically from header to main content to footer. 
4. 
5. This is your first accessible web page, ready to be viewed by anyone, including people using screen readers!

## Next Steps

Congratulations on finishing your accessible profile page! We've covered quite a lot in this tutorial. You've successfully:

1. Installed Visual Studio Code and configured it for accessibility
2. Set up the Live Server extension for real-time page previews
3. Written your first complete web page using HTML
4. Incorporated Bootstrap for consistent styling and layout
5. Created an accessible page structure with proper semantic elements
6. Learned how to use browser Developer Tools to inspect your work

In Part 2 of our three-part series, we'll add JavaScript to make the theme toggle button work, allowing users to switch between light and dark modes. Later, in Part 3, we'll cover how to deploy your page to make it available on the internet. 

Before moving on to the next articel, try adding more social media links to your page . For example, you could add links to Instagram, YouTube, or a personal blog. Use the same structure as the existing links and make sure to include descriptive text for each one. This will help reinforce what you've learned while personalizing your profile page even further.