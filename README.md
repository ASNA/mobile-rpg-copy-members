## ILE RPG /copy members

These /copy members provide reusable code for Mobile RPG applications. Unless otherwise stated, these members should be included at the end of the source. 

#### Assert 

Assert a condition and throw an *ESCAPE message if the condition isn't true. 

    alAssert(SQLSTT='0000', 'SQL call failed');

#### KeyMapF

Define INFDS data structure for determining what functions have been pressed by using position 360 of the INFDS. This method of determining function key presses has been discontinued for the newer INDDS data structure. 

#### Message
 
Display an info message (up to 75 characters long) usually used for test harnesses or debugging.

    alAssert('The SQLSTT value is:' + SQLSTT);

#### PgmBegin

Program initialization for Mobile RPG apps. (Include at beginning of program.)

#### Split

Routine to split a string into tokens. 

    Dcl-S splitResults   VarChar(100) Dim(10);

    Dcl-S Beatles VarChar(128);
    
    Beatles = 'John, George, Ringo, Paul';

    splitResults = alSplit(Beatles, ',');

    // splitResults now contains four elements: 
    // 1=John 2=George 3=Ringo 4=Paul

#### SQLHelpers

Procedures to help with embedded SQL.

