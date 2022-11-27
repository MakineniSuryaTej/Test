Book TABLE
|Field       |Type         |Null|Key|Default|Extra|
|------------|-------------|----|---|-------|-----|
|book_id     |varchar(8)   |NO  |PRI|null   |     |
|book_title  |varchar(30)  |YES |   |null   |     |
|category    |varchar(20)  |YES |   |null   |     |
|rental_price|decimal(10,2)|YES |   |null   |     |
|availability|varchar(5)   |YES |   |null   |     |
|book_author |varchar(30)  |YES |   |null   |     |
|publisher   |varchar(20)  |YES |   |null   |     |
------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------
Borrower TABLE
|Field       |Type         |Null|Key|Default|Extra|
|------------|-------------|----|---|-------|-----|
|borrower_id |varchar(10)  |NO  |PRI|null   |     |
|borrower_fname|varchar(20)  |YES |   |null   |     |
|borrower_lname|varchar(20)  |YES |   |null   |     |
|borrower_address|varchar(30)  |YES |   |null   |     |
|phone       |varchar(10)  |YES |   |null   |     |
|age         |int          |YES |   |null   |     |
------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------
Branch TABLE
|Field       |Type         |Null|Key|Default|Extra|
|------------|-------------|----|---|-------|-----|
|branch_id   |varchar(8)   |NO  |PRI|null   |     |
|branch_name |varchar(20)  |YES |   |null   |     |
|branch_address|varchar(30)  |YES |   |null   |     |
------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------
Copies TABLE
|Field       |Type         |Null|Key|Default|Extra|
|------------|-------------|----|---|-------|-----|
|book_id     |varchar(8)   |YES |MUL|null   |     |
|branch_id   |varchar(20)  |YES |MUL|null   |     |
|copies      |int          |YES |   |null   |     |
------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------
Issues TABLE
|Field       |Type         |Null|Key|Default|Extra|
|------------|-------------|----|---|-------|-----|
|issue_id    |varchar(8)   |NO  |PRI|null   |     |
|book_id     |varchar(8)   |YES |MUL|null   |     |
|branch_id   |varchar(8)   |YES |MUL|null   |     |
|borrower_id |varchar(10)  |YES |MUL|null   |     |
|dateout     |date         |YES |   |null   |     |
|datedue     |date         |YES |   |null   |     |
|datein      |date         |YES |   |null   |     |
------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------
Librarian TABLE
|Field       |Type         |Null|Key|Default|Extra|
|------------|-------------|----|---|-------|-----|
|librarian_id|varchar(8)   |NO  |PRI|null   |     |
|branch_id   |varchar(8)   |YES |MUL|null   |     |
|firstname   |varchar(20)  |YES |   |null   |     |
|lastname    |varchar(20)  |YES |   |null   |     |
|salary      |decimal(10,2)|YES |   |null   |     |
------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------