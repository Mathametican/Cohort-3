# Cohort-3
Hay gidi dünya
I am trying something new
text
// SELECT Account.Name, Id, FirstName, LastName, Phone, Email, Title, Department FROM Contact
List<Contact> get_contact = [SELECT Account.Name, 
                        Id, FirstName, LastName, Phone, Email, Title, Department 
                             FROM Contact];// flow get contact kısmı
for(Contact loopContact:get_Contact){
    System.debug(loopContact);
    System.debug('---------');
}
SELECT Account.Name, Id, FirstName, LastName, Phone, Email, Title, Department FROM Contact
