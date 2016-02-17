library (shiny)
ui <- fluidPage(
  titlePanel("Genera y grafica números aleatorios"),
  actionButton(inputId = "clicks", label="Genera datos"),
  plotOutput("grafica")
)

server <- function(input, output){
  datos <- eventReactive(input$clicks, {rnorm(100)})
  output$grafica <- renderPlot({plot(datos())})
}

shinyApp(ui=ui, server=server)
