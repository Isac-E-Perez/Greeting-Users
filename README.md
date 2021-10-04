# Greeting Users Project
### About: 

For this project, I implemented an application using Shiny-R. I used shiny to build the project. I created a simple code to greet the user thats on the application.

### Results:

First, I created the UI (User Interface) for the shiny application with a *fluidPage* layout.

![Screen Shot 2021-10-04 at 12 12 29 PM](https://user-images.githubusercontent.com/89553126/135894685-1d8ca136-fbf0-4bcf-8536-352b356619b1.png)

The UI is similar to the ingredients in a recipe. So lets list out the ingredients and what they do.

textInput lets the user create input unstructured text values.

textOutput renders a reactive output variable as text within an application page. textOutput() is usually paired with renderText().
 
Now lets focus on the server. The server is the directions in the recipe. The ingredients will be used as the directions describes them.

![Screen Shot 2021-10-04 at 12 20 42 PM](https://user-images.githubusercontent.com/89553126/135895807-3223a863-c351-4958-809a-481c219a9a08.png)

So lets list out the directions and what they do.

ouput$greeting variable is set to renderText which is paired with paste0 which concatenate all elements without separators and outputs the string hello and the inputted name .

input$name variable is set to the the users inputted string, in this case the user's name.

Finally, I write down the code shinyApp(ui, server) which constructs and starts the Shiny application from UI and server.

### Final Product:

![Screen Shot 2021-10-04 at 12 31 48 PM](https://user-images.githubusercontent.com/89553126/135897299-c6fbacd5-c50f-4784-9ffd-fe42d3cb5158.png)

![Screen Shot 2021-10-04 at 12 31 59 PM](https://user-images.githubusercontent.com/89553126/135897300-3dd45cfd-2e50-496d-b0ab-a363c8377c5c.png)
