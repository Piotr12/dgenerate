## Below are the instructions Cursor Composer received

Hey, I need you to create a static web app for me. Use something (maybe bootstrap) so it does look well without much effort. Single Page App please. 

The app is used to ease the Class Diagram creation for Mermaid JS. 

There are just a two feature: 

1) provided with a data tables definition it creates a Mermaid JS text output (class diagram) 
2) it renders this diagram 

The structure is a CSV format of below structure: 
Table;Column;Type;Key;NotNull;Comment;ReferenceTable;ReferenceColumn

For example 

Table;Column;Type;Key;NotNull;Comment;ReferenceTable;ReferenceColumn
Person;PersonID;Int;YES;YES;unique Person ID;;
Person;Name;String;NO;YES;name;;
Person;BirthDay;Date;NO;NO;;
Pet;PetID;Int;YES;YES;unique Pet ID;;
Pet;Name;String;NO;YES;pet name (e.g. 'Rex');;
Pet;OwnerID;Int;NO;YES;reference to person owning that pet;Person;PersonID

will create the following diagram 

classDiagram
    
    class Person{
      PK:Int ID
      String Name
      Date? Birthday  
    }
    class Pet{
      PK:Int PetID
      String Name
      Int OwnerID
    }
    Pet --> Person : OwnerID
    
Do note that non obligatory field is marked with ? character and the relation has the refrenced field name as a title. 