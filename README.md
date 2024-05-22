## Sabre

The Teneo Sabre Connector allows Teneo Developers to easily implement conversational experiences within the travel domain that are powered by Sabre APIs.  Travel Agencies can utilize the Teneo Sabre Connector in order to create online booking assistants for their agents and consumers.

The Teneo Sabre Connector includes a Teneo solution with pre-built flows handling different travel scenarios, like searching for flights, reviewing itineraries, getting specific details about a given itinerary and even booking a flight.  With the Teneo Sabre Connector, all these tasks can be achieved using natural language, which speeds up the booking process for agents and makes the customer experience extremely natural for end users.

In addition to pre-built flows, the Teneo Sabre Connector includes a Node.js application that acts as a backend mediator between Teneo and the Sabre APIs, facilitating the communication between both systems.  This application will give access to different Sabre API methods within the Air Booking workflow:
* Token Authentication (agency/developer authentication)
* Bargain Finder Max (searching for flights)
* Create Passenger Name Record (booking a flight)
* Get Booking (getting reservation details)

Thanks to this access, developers are able to implement not only the main conversational booking workflow, but also other follow-up questions like “Is there meal service onboard?”, “What is the distance between those two airports?” or “What is the duration of my flights?”.

Read more about Teneo: https://developers.teneo.ai/
Read more about Sabre: https://developer.sabre.com/guides/travel-agency/workflows/air-booking

## Deploying the Connector on Heroku

Click the button below to deploy the connector to Heroku:

[![Deploy](https://www.herokucdn.com/deploy/button.svg?classes=noborder)](https://heroku.com/deploy?template=https://github.com/delsolarvaldes/teneo-sabre-connector)

Copy your Teneo Sabre Connector endpoint from Heroku (e.g., https://teneo-sabre-connector.herokuapp.com)

## Running the Connector locally

1. Open a new terminal.
2. Clone this repository.
3. Navigate to your new "teneo-sabre-connector" repository --> cd teneo-sabre-connector
4. Start Node.js application --> npm start
* If this is the first time you are running the connector after cloning the repository, you may need to run "npm install"
5. Open another terminal and run ngrok --> ngrok http 3003

Copy your Teneo Sabre Connector endpoint from Ngrok (e.g., https://78d83402c15b.ngrok.io)

## Working with the Connector in Teneo Studio

1. Go to Teneo Developers.
2. Download your "Sabre Air Shopping Solution" solution file.
3. Import the solution into your Teneo Developers environment.
4. Save your Sabre developer details to the following Global Variables:
* sSabrePcc
* sSabreUserName
* sSabrePassword
5. Go to TryOut.
6. Set the following input parameter; value will be the Teneo Sabre Connector endpoint from your deployment above.
* For example --> sabre_connector_url = https://teneo-sabre-connector.herokuapp.com || https://78d83402c15b.ngrok.io
7. Start a session and test an input like: "I want to book a flight from Los Angeles to San Jose next Friday and returning the following week"
8. You should be all set to do some air shopping with Sabre!
