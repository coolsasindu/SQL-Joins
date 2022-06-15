# SQL-Joins product and supplier Table

```sql

-- Table structure for table `supplier`
--

CREATE TABLE IF NOT EXISTS `supplier` (
  `sid` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `Supplier_Name` varchar(45) NOT NULL DEFAULT '',
  `Office_Number` varchar(45) NOT NULL DEFAULT '',
  `Supplier_Email` varchar(45) NOT NULL DEFAULT '',
  `Billing_Address` varchar(245) NOT NULL DEFAULT '',
  `Shiping_Address` varchar(245) NOT NULL DEFAULT '',
  `City` varchar(45) NOT NULL DEFAULT '',
  `Product` varchar(45) NOT NULL DEFAULT '',
  `Bank` varchar(15) NOT NULL DEFAULT '',
  `Account_No` varchar(45) NOT NULL DEFAULT '',
  `Contact_Person` varchar(45) NOT NULL DEFAULT '',
  `Person_Email` varchar(45) NOT NULL DEFAULT '',
  `Mobile_Number1` varchar(45) NOT NULL DEFAULT '',
  `Mobile_Number2` varchar(45) NOT NULL DEFAULT '',
  `Online` varchar(45) NOT NULL DEFAULT '',
  `Other` varchar(45) NOT NULL DEFAULT '',
  `Private_Note` varchar(245) NOT NULL DEFAULT '',
  `Arrears_Balance` varchar(45) NOT NULL DEFAULT '',
  PRIMARY KEY (`sid`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=4 ;


--
-- Table structure for table `product`
--

CREATE TABLE IF NOT EXISTS `product` (
  `pid` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `Bar_Code` varchar(105) NOT NULL DEFAULT '',
  `Product_Name` varchar(45) NOT NULL DEFAULT '',
  `Category_Name` varchar(45) NOT NULL DEFAULT '',
  `Unit_Price` varchar(45) NOT NULL DEFAULT '',
  `Quantity` varchar(45) NOT NULL DEFAULT '',
  `Default_Type` varchar(45) NOT NULL DEFAULT '',
  `Type_Symbol` varchar(45) NOT NULL DEFAULT '',
  `Default_Unit` varchar(45) NOT NULL DEFAULT '',
  `Description` varchar(245) NOT NULL DEFAULT '',
  `MF_Date` varchar(45) NOT NULL DEFAULT '',
  `Exp_Date` varchar(45) NOT NULL DEFAULT '',
  `B_N` varchar(45) NOT NULL DEFAULT '',
  `sid` varchar(45) NOT NULL DEFAULT '',
  `Company_Name` varchar(45) NOT NULL DEFAULT '',
  `Brand_Name` varchar(45) NOT NULL DEFAULT '',
  `Private_Note` varchar(245) NOT NULL DEFAULT '',
  PRIMARY KEY (`pid`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=7 ;


# join Table in SID

SELECT product.pid, product.Product_Name, supplier.Supplier_Name
FROM product
INNER JOIN supplier ON product.sid=supplier.sid;

```
