# Definitions and Short Description  
**Global Application**: The whole project to which all teams participate.  
**Application**: The part of the **global application** this team works on.  
**Other Application/s**: The part of the **global application** other teams work on.  
**Gem Green**: `#99d447` *(hex)*  
**Financial-Hell Red**: `#f54c36` *(hex)*  
**Children**: Nested **UI Elements**.  
  
The **application** will have the following **UI Elements** (with additional information and short description):
- **Navbar**:
	- Navigation bar, enabling navigation between pages.
	- Present on the left side of all **UI Pages** except the **Stock Page** and the **Alert Windows**, shareing the viewport.
- **Portfolio**: 
	- Main **UI Page**.
	- Showcases basic information about the user's stocks.
- **Stock List**:
	- Showcases a list of all available stocks.
- **History**:
	- Showcases the history of transactions (related to stocks) the user has made.
- **Gem Store**:
	- Showcases a store where the user can buy **GEMS**, the currency of the **application**.
	- Interracts with one **other application** (*Andrada's Team*) for currency to currency exchange.
- **Alert Window/s**:
	- Popup Windows that showcase an alert related to a stock price.
- **Stock Menu**: 
	-  Showcases details and buy/sell information and abilities related to a stock.
	- Interracts with one **other application** (*Razvan's Team*) for sending alerts on buy/sell.
  
The **application** will have the following **NON-UI Elements** (with additional information and description):
- **Global Service**:
	- Will mainly manage: 
		- Seamless integration of all pages.
		- Direct communication with **other applications**. *(for encapsulation)*
		- State.
		- Defines the concepts of:
			-  **heart-beat**/s: the event of the new random generation of all values for all stocks *(in intervals of equal length of time)*.
			- **page change**: the request to change the current page to a diffrent one (specified in the request).
- **Database Wrapper**:
	- Will manage database connection and requests.
