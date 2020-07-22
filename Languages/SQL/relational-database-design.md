# Database Design

[Reference](https://www.dartmouth.edu/~bknauff/dewbd/2004-02/DB-intro.pdf)

## Terminology

- Anomalies: flaws that arise due to flaws in database design.

- Table || Relations
- Columns || Attributes
- Rows || Records || Tuples

- schema

- One-to-one, One-to-many, Many-to-one, Many-to-many

- Functional dependency: value in column B depends on a value in column A of a single table

- DBMS: database management system

### Keys
- Super Key: a set of columns that can identify a unique row in the table. A minimal super key is the smallest set of columns that can be used to identify a single row.
- Candidate Keys: possible colums (i.e. possible candidates) that can be used as a primary key
- Primary key: a column or set of columns that will be used to identify a single row from the table
- Foreign key: a column that is a primary key in another table [CHECK]

## Design principles
- Avoid lots of null values
- Avoid insertion/deletion/update anomalies
- Redundancy vs Loss of Data
- Design cycle: identify data->set data types->normalize tables/assign keys->rinse/repeat

### Types
- Strings: Not worth trying to determine exact length of string needed for text. 
Go for standard length sizes: varchar(n), where for 'text' n=4000 bytes,  
for a 'label' n=32 bytes, for a 'note' n=256 bytes.
    - if the requirements of string length are different, better not
    to handle it in the schema...do it in the logic layer of the app. 
    - be generous with how much space you give...always consider the largest possible case (and give a little more).
    - only use fixed-width strings (as opposed to text) for 
    codes (e.g. a code to represent the date-time) .. but note that sometimes
    the length of these get bigger 
    (e.g. look at the Y2K problem: where
    years that used to be represented by
    '99' for 1999 had to be changed to
    a 4 digit code e.g. '2000' in the year
    2000 instead of '00, due to problems that arose from the 2 digit code).
    - Text fields can hold alphanumeric information, including letters, numbers, spaces and punctuation marks.
    
- Numbers: just make sure its big enough
to support the range of values you want to store. 

- Timestamps (i.e. Date-Time): a standard exists to store these in SQL.

- Money: always store the currency along with the value of money (which should be stored as a decimal value...(need 5 to 9 digits)... note that you may need more than 2 decimal places (as many values carry more than 2 decimal places than for which the smallest coins exist in the currency...e.g. look at petrol pumps) - set up a different currency table for this.

- Complex data types: (examples:  phone numbers, postal addresses, contact information, and credit cards). These are often needed in many places. 
    - better to set up a different table for this and reference through foreign keys in other tables. 
    - e.g. for phone number, need a table with the following columns:
    CountryCode
    AreaCode
    ExchangeCode
    LineNumber
    Extension

- Other data types: (not all database programs support all of these)
    - currency
    - boolean
    - hyperlink
    - memo (for large quantities of text)
    - picture/object

- Store phone numbers as text not a number(As phone numbers can have non-numeric characters such as +44 (0)72203210)


### Normalisation of data
We aim to use the
least amount of storage space for our database while still maintaining all links between data. Additionally, a normalized DB schema avoids certain anomalies and so keep consistent data in the database.

Anomolies are the consequences of the redundancy introduced by improper or inadequate
separation between distinct entities.

They can help make your code which accesses the
database easier to understand, easier to expand upon, and in some cases, actually speed up your
application. 



### Other things to note
- sensitive data should be kept in database in encrypted form. (secret keys should not be kept in the database that allow you to decrypt the info)
- If database may be used internationally -- consider: storing more than one language, regional differences (phone numbers, currency, etc.). Use a DBMS capable of handling multi-byte characters.
- Column names shouldn't have spaces.
- Database will format and validate the data a little depending on the types you have selected. However, always pre-validate all data before presenting it to the database (on the client-side or server-side).

## TO LOOK UP
- advanced data
access technologies such as ADO (ActiveX Data Objects)
