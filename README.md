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
public class PerimeterCalculation {
  Public  Integer perimeter;                                          // Değişken STATIC se METOD da STATIC olmalı 
    Public  Integer perCalc(Integer a, Integer b, Integer c){         // Değişken NON-STATIC ise METOD da NON-STATIC olmalı
          perimeter= a+b+c;                                            
          System.debug('Perimeter of Triangle   '+perimeter);          
          return perimeter;                                            
          }                                                          
    Public  Integer PerCalc(Integer a, Integer b, Integer c, Integer d){  
        perimeter=a+b+c+d;                                                      
        System.debug('Perimeter of Rectangle   '+perimeter);
        return perimeter;
    }


}
public class Cars {
    //Properties
    private Integer model;                       // private olunca METOD ile bilgi girişi yapıyoruz.
    private String  color;
    private String  packet;
    private Integer maxSpeed;
    private Integer speed;
    private Integer brake=0;                     // Burada variable/ propertieslere default bir deger atandı. Durgunken ki araba hızı fren gibi
    
    //Setter Metod                               // Private olduğu için sistemde bu variable/properties lere bilgi girişini 
    public void setModel(Integer model){         // SETTER METOD ile yapacağız.   metod ismi SET ile başkamak zorunda değil sadece hatırlatıcı
       this.model=model;                         //olsun diye öyle yaptık.
    }                                            // Private olan model variable na this. ön eki ekleyip model olarak tanımladığımız setter Motod a 
                                                 // eşitledik.
    public void setColor(String color){
        this.color=color;
    }
    public void setpacket(String packet){
        this.packet=packet;
        
    }
    public void setMaxSpeed(Integer maxSpeed){
        this.maxSpeed=maxSpeed;
    }
    public void setspeed(Integer speed){
        this.speed=speed;
    }
    public void setbrake(Integer brake){
        this.brake=brake;
    }
    // Getter Metod
    public Integer getModel(){                     // Adı üstünde bir şey döndüreceği için bunu void değil Integer bir type ile tanımladık
        return model;                              // ne getireceği belli olduğu için () parametre tanımlamadık 
    }                                              // Type Integer bundan dolayı RETURN dedik.
    public String getColor(){
        return color;
    }
    public String getPacket(){
        return packet;
    }
    public Integer getMaxSpeed(){
        return maxSpeed;
    }
    public Integer getspeed(){
        return speed;
    }
    public Integer getBrake(){
        return brake;
    }
    public void run(){                                         // run metodu tanımladık araba çalıştı.                  
        System.debug('The vehicle is running');
    }
    public void stop(){                                        // stop metodu tanımladık araba durdu.
        system.debug('The vehicle is stopped');
    }
    public Integer acceleration(Integer accelerate){           // accelaration metod tanımladık hız için;
        speed = accelerate + speed;                            // speed i burada yeniden tanımladık bu Metod için
        // buda aynı şey 
        // speed +=accelerate
        if(speed<maxSpeed){                                   // burayada speed maxSpeed geçemez diye IF ile şart koştuk.
            System.debug('Current Speed  '+speed);
        }else{
            System.debug('Curent Speed  '+maxSpeed);
        }                                     
        return speed;
    }
    public Integer brake (Integer brake){                    // burada frene basma için Metod tanımladık.
        speed = speed - brake;                               // burada speed i bu metod için yeniden tanımladık.                            
        if(speed>0){
            System.debug('Current Speed  '+speed);
        }else{
           // şöylede yapabilirdik. speed=0 system.debug('Current Speed  '+speed); 
            System.debug('Current Speed  =0 ');
        }
        return speed; 
    }
    
}public class Cars {
    //Properties
    private Integer model;                       // private olunca METOD ile bilgi girişi yapıyoruz.
    private String  color;
    private String  packet;
    private Integer maxSpeed;
    private Integer speed=0;
    private Integer brake=0;                     // Burada variable/ propertieslere default bir deger atandı. Durgunken ki araba hızı fren gibi
    
    //Setter Metod                               // Private olduğu için sistemde bu variable/properties lere bilgi girişini 
    public void setModel(Integer model){         // SETTER METOD ile yapacağız.   metod ismi SET ile başkamak zorunda değil sadece hatırlatıcı
       this.model=model;                         //olsun diye öyle yaptık.
    }                                            // Private olan model variable na this. ön eki ekleyip model olarak tanımladığımız setter Motod a 
                                                 // eşitledik.
    public void setColor(String color){
        this.color=color;
    }
    public void setpacket(String packet){
        this.packet=packet;
        
    }
    public void setMaxSpeed(Integer maxSpeed){
        this.maxSpeed=maxSpeed;
    }
    public void setspeed(Integer speed){
        this.speed=speed;
    }
    public void setbrake(Integer brake){
        this.brake=brake;
    }
    // Getter Metod
    public Integer getModel(){                     // Adı üstünde bir şey döndüreceği için bunu void değil Integer bir type ile tanımladık
        return model;                              // ne getireceği belli olduğu için () parametre tanımlamadık 
    }                                              // Type Integer bundan dolayı RETURN dedik.
    public String getColor(){
        return color;
    }
    public String getPacket(){
        return packet;
    }
    public Integer getMaxSpeed(){
        return maxSpeed;
    }
    public Integer getspeed(){
        return speed;
    }
    public Integer getBrake(){
        return brake;
    }
    public void run(){                                         // run metodu tanımladık araba çalıştı.                  
        System.debug('The vehicle is running');
    }
    public void stop(){                                        // stop metodu tanımladık araba durdu.
        system.debug('The vehicle is stopped');
    }
    public Integer acceleration(Integer accelerate){           // accelaration metod tanımladık hız için;
        speed = accelerate + speed;                            // speed i burada yeniden tanımladık bu Metod için
        // buda aynı şey 
        // speed +=accelerate
        if(speed<maxSpeed){                                   // burayada speed maxSpeed geçemez diye IF ile şart koştuk.
            System.debug('Current Speed  '+speed);
        }else{
            System.debug('Curent Speed  '+maxSpeed);
        }                                     
        return speed;
    }
    public Integer brake (Integer brake){                    // burada frene basma için Metod tanımladık.
        speed = speed - brake;                               // burada speed i bu metod için yeniden tanımladık.                            
        if(speed>0){
            System.debug('Current Speed  '+speed);
        }else{
           // şöylede yapabilirdik. speed=0 system.debug('Current Speed  '+speed); 
            System.debug('Current Speed  =0 ');
        }
        return speed; 
    }
    
}
public class MathC {
    public static void minimum(integer a,integer b,integer c){
        if(a<Math.min(b,c)){
            System.debug(a);
            
    } else {
        System.debug(Math.min(b,c));
       
    }
    }
}  
public class MathC {
public static integer x;
public static Double sayi;
public static Double gelen(){
 sayi = Math.random()*100;
  x=Integer.ValueOf(sayi);
   System.debug(x);
   return x;
   }
    public static void Tahmin(Integer y){
    if(x==y){
             System.debug('Tahmininiz Doğru Kazandınız.');
    }else if(y<0||y>100){
             System.debug('Lütfen 0 ile 100 arasında bir sayı giriniz.');
    }else{
    System.debug('Tekrar deneyiniz. Bilgisayarın tutugu sayı   :'+x);
                    }
}
Opportunity opp1 = New Opportunity(
    Name = 'New Opportunity Apex Hours 0213',
    Amount= 5000,
    CloseDate=date.today(),
    StageName='Prospecting'
   );
Opportunity opp2=New Opportunity(
    Name = 'New Opportunity Apex Hours 0223',
    Amount= 3000,
    CloseDate=date.today(),
    StageName='Prospecting'
   );
List<Opportunity> opplist=New List<Opportunity>{opp1,opp2};
insert opplist;
Opportunity opp1 = New Opportunity(
    Name = 'New Opportunity Apex Hours 0213',
    Amount= 5000,
    CloseDate=date.today(),
    StageName='Prospecting'
   );
Opportunity opp2=New Opportunity(
    Name = 'New Opportunity Apex Hours 0223',
    Amount= 3000,
    CloseDate=date.today(),
    StageName='Prospecting'
   );
List<Opportunity> opplist=New List<Opportunity>{opp1,opp2};
    Database.SaveResult[] sr = database.insert(opplist,false);
for(database.SaveResult var : sr){
   System.debug('Result : '+var.isSuccess()) ;
}Account Acc = New Account(
   Name= 'Test Account 0213'
);
   insert Acc;
Account accQuery = [SELECT Id FROM Account WHERE Name ='Test Account 0213'];
System.debug('------'+accQuery);
Contact con = New Contact(
  LastName= 'Contact'      
);
insert con;

Account Acc = New Account(
   Name= 'Test Account 0213'
);
   insert Acc;
Account accQuery = [SELECT Id FROM Account WHERE Name ='Test Account 0213'];
System.debug('------'+accQuery);

System.SavePoint svp = Database.setSavePoint();

try{
    Contact con = New Contact(
  LastName= 'Contact'      
);
    insert con;
}catch(Exception ex){
    Database.rollback(svp);
}
public class Kitap {
    public static void Kayit(string a, string b , string k){
        yay_nevi__c x=New yay_nevi__c();
        x.Name= a;
        insert x;
        
        yazar__c y=New yazar__c();
        y.name=b;
        y.yay_nevi__c=x.Id;
        insert y;
        
        kitap__c z=New kitap__c();
        z.name=k;
        z.yazar__c=y.Id;
        insert z;
    }
}

LIST<LIST<SObject>> x=[FIND ' de' IN Name FIELDS 
                       RETURNING Account, Contact, Opportunity]; 

for(integer i=0; i<x.size();i++){
   System.debug(x); 
}

LIST<LIST<SObject>> y=[FIND 'ab' IN Name FIELDS 
                       RETURNING kitap__c, yazar__c, yay_nevi__c]; 

for(integer i=0; i<y.size();i++){
   System.debug(y); 
}
LIST<LIST<SObject>> x=[FIND ' de' IN Name FIELDS 
                       RETURNING Account, Contact, Opportunity]; 

System.debug(x.get(0));
System.debug(x.get(1));


public class StringArrayTest {
    public static void generateStringArray(integer n){
               String y='Test';
        list<String> x= New List<String>();{
            for(integer i=0; i<n; i++){
                 x.add(y+i);
                 }
            System.debug(x);
        }
    }
}

List<Account> MultiAcc= New List<Account>();
for(integer num=0; num<=300; num++){
    Account singleAcc = New Account();
    singleAcc.Name='Bulk Acc-APEX'+num;
    multiAcc.add(singleAcc);
}
   
Account singleAccError = New Account();
singleAccError.phone= '234 234 234 34';
multiAcc.add(singleAccError);

//indert multiAcc; Database.insert(multiAcc,true);

//List<Database.SaveResult>
Database.SaveResult[] srList= Database.insert(multiAcc,false);

for(Database.SaveResult sr:srList){
    if(sr.isSuccess()){
//Operation was successfully, so get the ID of the record that was processed
    System.debug('Successfully inserted account. Account ID  :'+sr.getId());
    }else{
// Operation failed, so get all errors
        for(Database.Error err:sr.getErrors()){
         System.debug('The following error has occured.');
         System.debug(err.getStatusCode()+'  :  '+err.getMessage());
         System.debug('Account fields that affected this error: '+err.getFields());
        }
    }
}

Account acct= new Account( name='Acme', phone='(415)555-1212',NumberOfEmployees=100);
insert acct;
ID acctId= acct.Id;
system.debug('ID :'+acctId);
// burada yeni insert edilen bir record un ID si ni getiriyoruz.

public class Lab1 {
    public static void LoopKontrol(){
        integer i;
        double sum=0.0;
    for( i=1; i<=10; i++){
        System.debug(i);
        sum+=i;
        }
    System.debug('Sum :'+sum);
    }

}