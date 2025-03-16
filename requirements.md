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
			- **page change**: the request to change the current page to a different one (specified in the request).
- **Database Wrapper**:
	- Will manage database connection and requests.


# Navbar *- Ionut*
A side-bar navigation menu enabling navigation between pages. Present on the left side of all **UI Pages** except the **Stock Page** and the **Alert Window**.    
The navbar will have the following **UI Elements**, displayed **vertically** from top to bottom in the following order:
- **Container - Wallet:**
	- All applied style is not required by the requirement but welcome. 
	- Horizontally spanning the whole navbar width. **(FILL)** 
	- Vertically spanning the height of the content. **(FIT)**
	- **Children** are alligned **vertically**.
	- Contains the following **UI Elements**:
		- **Text Label** displaying the user's **username**
			- All applied style is not required by the requirement but welcome.
		- **Text Label** displaying the text **"Gems: "**, followed by the amount of **gems** the user currently posseses.
			- **Gem Green** colored Text (any shade).
			- Other applied style is not required by the requirement but welcome.
			- The text should refresh every time the amount of gems the user possesses changes to reflect the new value.
		- **Text Label** displaying the text **"Stocks (as Gems): "** followed by the current *'market value'* of all the stocks possesed by the user.
			- All applied style is not required by the requirement but welcome.
			- The value should be re-calculated every **heart-beat** with the new data provided by the **Global Service** and refreshed in the ui to reflect the new value.
- **Button** displaying the text **"Portfolio"**.
	- Horizontally spanning the whole navbar width. **(FILL)** 
	- Vertically spanning the height of the content. **(FIT)**
	- If the **current page** is the one indicated by the button, the background color of the button should be **Gem Green**.
	- Other applied style is not required by the requirement but welcome.
	- When clicked request from **global service** *page change* to the **Portfolio** page.
- **Button** displaying the text **"Stocks"**.
	- Horizontally spanning the whole navbar width. **(FILL)** 
	- Vertically spanning the height of the content. **(FIT)**
	- If the **current page** is the one indicated by the button, the background color of the button should be **Gem Green**.
	- Other applied style is not required by the requirement but welcome.
	- When clicked request from **global service** *page change* to the **Stock List** page.
- **Button** displaying the text **"History"**.
	- Horizontally spanning the whole navbar width. **(FILL)** 
	- Vertically spanning the height of the content. **(FIT)**
	- If the **current page** is the one indicated by the button, the background color of the button should be **Gem Green**.
	- Other applied style is not required by the requirement but welcome.
	- When clicked request from **global service** *page change* to the **History** page.
- **Button** displaying the text **"Gem Store"**.
	- Horizontally spanning the whole navbar width. **(FILL)** 
	- Vertically spanning the height of the content. **(FIT)**
	- If the **current page** is the one indicated by the button, the background color of the button should be **Gem Green**.
	- Other applied style is not required by the requirement but welcome.
	- When clicked request from **global service** *page change* to the **Gem Store** page.
