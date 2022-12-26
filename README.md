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
List<Account> mylist=[SELECT  Id, Name FROM Account];// BURADA tüm Account ları getirdik
                                                     // Çünkü  tüm listeyi dolaşım silmemiz istenen
                                                     // degeri siliyor yoksa Loop içinde DML kullanmış olursun.
List<Account> a=new List<Account>();                 // silinmesini istediğimiz verileri buraya atacak
for(Account y:mylist){                               // bunu if else ile yapacağız.
    if(y.Name=='Company  6'){
            a.add(y);                                // add bir modül yani .add() şeklinde yazılmalı
    }
}                                                    // sonrada bu listeyi sileceğiz
delete a; 
List<Account> IsdltdList=[SELECT Id, Name, IsDeleted FROM Account WHERE  Name LIKE '%Company%' All Rows];
// All ROWS kodunu ekleyerek silen verileri de getiriyoruz.
List<Account> a=New List<Account>();                         // silinen verileri bu listeye if koşulu ile ekliyoruz 
for(Account x:Isdltdlist){                                   // For döngüsü ile Isdltdlist teki verileri tek tek 
    if(x.Isdeleted==True){                                   // kontrol ediyor If ile oluşturulan şartları sağlarsa
        a.add(x);                                            // a listesine ekleniyor. Amaç DML loop içinde kullanmamak
    }  
}  undelete a;                                              // Undelete ilede daha önceden sildiğim verileri geri getirdim. 