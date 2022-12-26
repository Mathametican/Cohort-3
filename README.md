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
public class PerimeterCalculation {
  Public static Integer perimeter;                                      // çevre hesabı yapacak bir değişken tanımlandı.Variable Properties
    Public static Integer perCalc(Integer a, Integer b, Integer c){     // bu variable için bir METOD tanımlıyoruz.// Integer type RETURN gerekli
          perimeter= a+b+c;                                             // METOD İÇİNDE tanımladıklarımız parametre
          System.debug('Perimeter of Triangle   '+perimeter);           // Burada Class içinde System.debug tanımladık CODE kımında 
          return perimeter;                                             //yazmaya gerek olmasın
          }                                                          
    Public static Integer PerCalc(Integer a, Integer b, Integer c, Integer d){  // Aynı isimle farklı body de Metod TANIMLADIK üçlü mü dörtlümü
        perimeter=a+b+c+d;                                                      // o ayırabilecek.
        System.debug('Perimeter of Rectangle   '+perimeter);
        return perimeter;
    }


}