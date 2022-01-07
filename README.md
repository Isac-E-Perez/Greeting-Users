# Greeting Users Project
### About: 

For this project, I implemented an application using Shiny-R. I used shiny to build the project. I created a simple code to greet the user thats on the application.

### Results:

First, I created the UI (User Interface) for the shiny application with a *fluidPage* layout.

```R
library(shiny)  # calls from library shiny
# user interface: defines how the application looks 
# fluidPage: creates the page with a fluid layout 
ui <- fluidPage(
  # textInput(inputId, label, value = "")
  # Create an input control for entry of unstructured text values
  textInput("name", "What is your name?"),
  
  # textOutput(outputId, container = if (inline) span else div, inline = FALSE)
  # Render a reactive output variable as text within an application page. 
  #textOutput() is usually paired with renderText() and puts regular text in 
  #<div> or <span>
  textOutput("greeting")
)
```

The UI is similar to the ingredients in a recipe. So lets list out the ingredients and what they do.

textInput lets the user create input unstructured text values.

textOutput renders a reactive output variable as text within an application page. textOutput() is usually paired with renderText().
 
Now lets focus on the server. The server is the directions in the recipe. The ingredients will be used as the directions describes them.

```R
server <- function(input, output, session){
  output$greeting <- renderText({
    # paste0: used to concatenate all elements without separator. 
    paste0("Hello ", input$name)
  })
}
# to construct and start a Shiny application from UI and server.
shinyApp(ui, server)
```

So lets list out the directions and what they do.

ouput$greeting variable is set to renderText which is paired with paste0 which concatenate all elements without separators and outputs the string hello and the inputted name .

input$name variable is set to the the users inputted string, in this case the user's name.

Finally, I write down the code shinyApp(ui, server) which constructs and starts the Shiny application from UI and server.

### Final Product:

![Screen Shot 2021-10-04 at 12 31 48 PM](https://user-images.githubusercontent.com/89553126/135897299-c6fbacd5-c50f-4784-9ffd-fe42d3cb5158.png)

![Screen Shot 2021-10-04 at 12 31 59 PM](https://user-images.githubusercontent.com/89553126/135897300-3dd45cfd-2e50-496d-b0ab-a363c8377c5c.png)
