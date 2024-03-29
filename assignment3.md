# Assignment 3 For CMSI 486: Databases

## MongoDB
### 1.
**Query:** show collections

**Result:**\
categories\
customers\
employee-territories\
northwind\
order-details\
orders\
products\
regions\
shippers\
suppliers\
territories


### 2.
**Query:** db.categories.count()

**Result:** 8

### 3.
**Query:** db.orders.count()

**Result:** 830

### 4.
**Query:** db.orders.count( {EmployeeID: 8} )

**Result:** 104

### 5.
**Query:** db.employees.find( { EmployeeID: 1 }, { _id: 0, LastName: 1 } )

**Result:** { "LastName" : "Davolio" }

### 6.
**Query:** db.orders.distinct( "EmployeeID", { "OrderID": { $lt: 10300 } } )

**Result:** [ 5, 4, 3, 9, 1, 8, 6, 2, 7 ]

### 7. 
**Query:** db.suppliers.distinct( "CompanyName" )

**Result:** [  
	"New Orleans Cajun Delights",  
	"Grandma Kelly's Homestead",  
	"Tokyo Traders",  
	"Cooperativa de Quesos 'Las Cabras'",  
	"Mayumi's",  
	"Pavlova",  
	"Specialty Biscuits",  
	"PB Knäckebröd AB",  
	"Refrescos Americanas LTDA",  
	"Heli Süßwaren GmbH & Co. KG",  
	"Plutzer Lebensmittelgroßmärkte AG",  
	"Nord-Ost-Fisch Handelsgesellschaft mbH",  
	"Exotic Liquids",  
	"Formaggi Fortini s.r.l.",  
	"Norske Meierier",  
	"Bigfoot Breweries",  
	"Aux joyeux ecclésiastiques",  
	"Svensk Sjöföda AB",  
	"Leka Trading",  
	"Lyngbysild",  
	"Zaanse Snoepfabriek",  
	"Karkki Oy",  
	"Pasta Buttini s.r.l.",  
	"Escargots Nouveaux",  
	"Gai pâturage",  
	"G'day",  
	"Ma Maison",  
	"New England Seafood Cannery",  
	"Forêts d'érables"  
]  

### 8. 
**Query:** db.suppliers.count()

**Result:** 29

### 9. 
**Query:**: db.suppliers.find( { City: "Boston" }, { _id: 0, SupplierID: 1, Phone: 1 } )

**Result:** { "SupplierID" : 19, "Phone" : "(617) 555-3267" }

### 10. 
**Query:** db.orders.aggregate( [ { $group : { _id : "$EmployeeID", count : { $sum : 1 } } }, { $sort : { count : -1 } }, { $limit : 1 } ] )

**Result:** { "_id" : 4, "count" : 156 }

### 11. 
**Query:** db.territories.aggregate( [ { $match: { "RegionID": 2 } }, { $group : { _id : {"TerritoryDescription": "$TerritoryDescription"} } }, { $group : { _id : null, count : { $sum: 1 }, results : { $push: "$$ROOT" } } } ] )

Result: { "_id" : null,  
"count" : 15,  
"results" : [ { "_id" : { "TerritoryDescription" : "Seattle" } },  
{ "_id" : { "TerritoryDescription" : "Bellevue" } },  
{ "_id" : { "TerritoryDescription" : "SantaCruz" } },  
{ "_id" : { "TerritoryDescription" : "SantaClara" } },  
{ "_id" : { "TerritoryDescription" : "Campbell" } },  
{ "_id" : { "TerritoryDescription" : "MenloPark" } },  
{ "_id" : { "TerritoryDescription" : "Scottsdale" } },  
{ "_id" : { "TerritoryDescription" : "SantaMonica" } },  
{ "_id" : { "TerritoryDescription" : "Phoenix" } },  
{ "_id" : { "TerritoryDescription" : "ColoradoSprings" } },  
{ "_id" : { "TerritoryDescription" : "SanFrancisco" } },  
{ "_id" : { "TerritoryDescription" : "HoffmanEstates" } },  
{ "_id" : { "TerritoryDescription" : "Denver" } },  
{ "_id" : { "TerritoryDescription" : "Redmond" } },  
{ "_id" : { "TerritoryDescription" : "Chicago" } } ] }

### 12. 
**Query:** db.shippers.find( { CompanyName: "United Package" }, { _id: 0, Phone: 1 } )

**Result:** { "Phone" : "(503) 555-3199" }

## Neo4j

### 1. 
**Query:** CALL db.labels() YIELD label RETURN label

**Result:**
"label"
"Customer"
"Product" 
"Supplier" 
"Employee" 
"Category" 
"Order"    
"Territory"
"Shipper" 
"Orders"  
"Suppliers"

### 2. 
**Query:** MATCH (n:Category) RETURN count(n)

**Result:** 
"count(n)"
8

### 3. 
**Query:** MATCH (n:Order) RETURN count(n)

**Result:**
"count(n)"
830

### 4. 
**Query:** MATCH (n:Orders) WHERE n.EmployeeID = '8' RETURN count(n)

**Result:**
"count(n)"
104

### 5. 
**Query:** MATCH (n:Employee) WHERE n.employeeID = '1' RETURN n.lastName

**Result:**
"n.lastName"
"Davolio"

### 6. 
**Query:** 

**Result:**

### 7. 
**Query:**

**Result:**


### 8. 
**Query:** MATCH (n:Supplier) RETURN count(n)

**Result:**
"count(n)"
29

### 9. 
**Query:** MATCH (n:Suppliers) WHERE n.City = 'Boston' AND n.Region = 'MA' RETURN n.SupplierID, n.Phone

**Result:**
"n.SupplierID"    "n.phone"
19		"(617) 555-3267"

### 10. 
**Query:** 

**Result:**

### 11. 
**Query:** 

**Result:**

### 12. 
**Query:** MATCH (n:Shipper) WHERE n.companyName = "United Package" RETURN n.phone

**Result:**
"n.phone"
(503) 555-3195






