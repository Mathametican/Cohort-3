# Cohort-3
write something new
List<Account> deleteList=[SELECT  Id, Name FROM Account WHERE Name LIKE '%Company%'];
                                         // Silecegim veri Account List ile çagırdım.
for(Account dltl:deletelist){
    System.debug(dltl);                  // for döngüsü ile listedeki verileri ayrı ayrı  
           Delete dltl;
}  
List<Account> deleteList=[SELECT  Id, Name FROM Account WHERE Name LIKE '%Company%'];
                                         // Silecegim veri Account List ile çagırdım.
Delete deletelist;                       // for döngüsü içerisine yazmadan da silebiliyoruz.