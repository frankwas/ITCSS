# ITCSS
ITCSS repo that follows ITCSS standards

# What is it?
ITCSS is a scalable and maintanable CSS Architecture made popular by Lubos Kmetko. It helps to create a "upside pyramid" structure for your CSS that allows you to easily scale your code up and down as needed. I have used it on small to very large enterprise applications. Not only does it help you organise your code better, it makes it super efficient.

# The Upside Pyramid
##### ITCSS is split into 7 levels as follows:
1. Settings : used with preprocessors and contain font, colors definitions, etc.
2. Tools : globally used mixins and functions. It’s important not to output any CSS in the first 2 layers.
3. Generic : reset and/or normalize styles, box-sizing definition, etc. This is the first layer which generates actual CSS.
4. Elements : styling for bare HTML elements (like H1, A, etc.). These come with default styling from the browser so we can redefine them here.
5. Objects : class-based selectors which define undecorated design patterns, for example media object known from OOCSS
6. Components : specific UI components. This is where majority of our work takes place and our UI components are often composed of Objects and Components
7. Utilities : utilities and helper classes with ability to override anything which goes before in the triangle, eg. hide helper class

# How to use it
I have created some sample files in the folder structure. But you can add as many as you need for your project. Just make sure that every new file that you create has a corresponding import in the **index.scss** file. This is very important otherwise your CSS will not be loaded. Other than that, you can use it as any other SCSS file that needs to compile. You only need to compile the index file as this should pull in all imports as long as it's at the root of your folder where these 7 folders are its children.
