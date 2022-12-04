# Spring-Boot-Turkish-Notes


## Spring Nedir?

- Spring popüler bir Java frameworküdür.

## Spring Kütüphanesi
- Spring; bir web uygulaması geliştirmek için en yaygın olarak kullanılan Java EE (Java Enterprise Edition) kütüphanelerinden biridir. Java platformu için ayrıntılı bir programlama ve yapılandırma modeli sunar. Java EE kapsamında uygulama geliştirmeyi basitleştirmeyi amaçlar ve biz geliştiricilerin daha üretken olmasına yardımcı olur.
- Spring kütüphanesinin en önemli özelliği Dependency Injection dır. 
- Spring kütüphanesi bize esneklik uygulamaya odaklanırken, Spring Boot kod uzunluğunu kısaltmayı ve bir web uygulaması geliştirmenin en kolay yolunu bize sunmayı amaçlamaktadır.

![image](https://user-images.githubusercontent.com/61595808/205480333-e1a50a03-e958-40f5-876a-85c4ba29accd.png)

 Bu resim için linkteki videoya bak    https://www.fusion-reactor.com/blog/the-difference-between-spring-framework-vs-spring-boot/
 
 
 ![image](https://user-images.githubusercontent.com/61595808/205480620-87f6a5f2-dba2-4e5a-992b-8844d0538153.png)


![image](https://user-images.githubusercontent.com/61595808/205480865-ab9ae2ee-f9d7-4a48-905a-2387c8bf9609.png)


## Tomcat Nedir?

- Web sunucusudur.

## IoC(Inversion of Control)

- Bir yazılım tasarım prensibidir.
-  Ioc ile Uygulama içerisindeki obje instance’larının yönetimi sağlanarak, bağımlılıklarını en aza indirgemek amaçlanmaktadır.
- Yazdığımız kod bloğu çalışacağı zaman, framework bizim kodumuzu çağırır ve çalıştırır daha sonra kontrol yeniden framework’e geçmesi olayının tümüne Inversion Of Control adı verilmektedir.

![image](https://user-images.githubusercontent.com/61595808/205481037-c0f92a98-743f-4ac7-822e-5f3a6784b987.png)


## Spring Bean nedir?

 - Java objesidir.
 
## NOT : Önceden XML ile her şeyi yani beanleri teker teker yazılıyormuş.

## Dependency Injection
 
- Mesela ben araba almak istiyorum benim gerçektende bir araba yapmama gerek yok. Dependency Injection ise bu işlemi yapıyor.
-  dependency = helper objects
- Injection Types : En yaygın olan ikisi şunlardır: Constructor Injection ve Setter Injection.
- Dependency Injection'ı ise  @Autowiring ile sağlıyoruz.

## Java Annotations

- @ kullanarak gerçekleştirilir.
- Mesela @Autowiring ile dependency injection yaparız , ya @Id  diyerek id olduğunu belirtiriz.

## Autowiring Injection Types

- Constructor Injection
- Setter Injection
- Field Injections

## @Component nedir?

- Bir sınıfı “Bean” olarak işaretler. (spring tarafından yönetilen bean)
- Örnek olarak da @ComponentScan("package ismini buraya yazarız")

## @Configuration nedir?

- @Bean tanımlaması içeren fonksiyonlar içerir.
- Tanımlandığı fonksiyon her neyi return ediyorsa, onun context içine ekleneceğini belirtir.
- @Bean, genelde 3rd parti sınıflar context içine eklenmek istediğinde kullanılır. 
- Dosya içerisinden birden çok bean tanımı olabileceğini belirtir.

## Spring MVC

- Spring MVC Java da web projeleri için kullanılanılır.
- Model View Controller, Design Pattern'a dayalıdır

![image](https://user-images.githubusercontent.com/61595808/205362688-f592ad58-6933-4101-91b3-6fcceaac9957.png)

#### Controller

- Kodlar geliştiriciler tarafındna oluşturulur
- Uygun view templateları gönderir

#### Model

- Model: data'yı içerir

#### View

- Spring Mvc flexibledır,bir çok template i içerir. En yaygın olanları JSP(Java Server Pages) Vve JSTL(JSP Standart Tag)'dır.
- Diğer destekledikleri ise Thymeleaf, Groovy etc

## @RequestMapping("/.....")

- Template de  "..." bu kısım bizim 
- form action=" ....." karşılık gelen kısımdır.
- form action=" ....."  method="GET"> ---  </form>
- Ya da class bilgisinden öncede kullanabiliyoruz. Bunada "parent mapping" deniliyor.

## @RequestParam()

- Attribute ismini yazarız
  
## Data Binding
  
![image](https://user-images.githubusercontent.com/61595808/205450562-045fae5f-c6db-4c3a-aa36-35b1a8059bec.png)

## Form Validation 

- Validation Annotations : @NotNull, @Min, @Max, @Size etc

## Binding Result

- Verilerin gönderimi sırasında oluşan hata ve bilgilere erişim BindingResult ve Errors arayüzünde yer alan metotlar ile yapılır.

## Hibernate Nedir?

- Hibernate, Java platformunda yazılmış bir ORM aracıdır. ORM, nesne odaklı dillerdeki nesnelerin, ilişkisel veri tabanlarındaki kayıtlara nasıl karşılık geldiğini yürüten bir teknolojidir.
-  Java Code <---> Hibernate <----> Database
- SQL, JDBC ,ORM(Object To Relational )
- Hibernate uses JDBC for all database communications.

   Java App <----> Hibernate    JDBC  <----> Database
   
## Why we are using JPA Annotations instead of Hibernate?

- Jpa is a standard specification. Hibernate  is an implementation of the JPA specification.
- Hibernate implementations all of JPA annotations.
- The Hibernate team recommends the use of JPA Annotations as a best practice.

## Spring Data JPA ile örnek kodlama

- Spring Data Jpa ile CRUD operasyonları için herhangi bir implementasyon yazmanıza gerek yoktur.
-  repo.findAll(); Bu kod bloğu ile tablodaki tüm kayıtlar listelenecek.
-  Hibernate ise nesneleri ilişkisel veritabanlarında kalıcı hale getirmenize olanak tanıyan bir nesne-ilişkisel eşleme aracıdır.
-  Jpa sadece bir standart ,hibernate onu implemente ediyor.

## ID Generation  Strategies

- GenerationType.AUTO/IDENTIFY/SEQUENCE/TABLE  

## Hibernate Query Language(HQL)

## One-to-One
## One-to-Many , Many-to-One
## Many-to-Many


## Entity Lifecycle

![image](https://user-images.githubusercontent.com/61595808/205453073-273f873d-4a24-4bb2-b56f-6cead2c711ae.png)



## @OnetoOne - Cascade Types

![image](https://user-images.githubusercontent.com/61595808/205453142-de21245a-dee6-4315-9582-eb03efbb6c05.png)


![image](https://user-images.githubusercontent.com/61595808/205453191-9f67960e-ef1c-4600-9b14-f9cefa1b93b4.png)

![image](https://user-images.githubusercontent.com/61595808/205486296-1723ae7e-cab9-41dd-ad52-c81bb817d791.png)



## Cascade 

- Cascade JPA standartıdır. Java sınıflarımızdaki ilişkilerin davranışlarını cascade niteliğini kullanarak ayarlarız. 
- “İlişki davranışları” kavramını biraz açıklayacak olursak, bir değer silinirse o veri ile ilişkili olan kayıtların etkilenmesini ya da etkilenmemesi işlemlerini Java nesneleri olarak yönetilmesini sağlamaktayız. Bu JPA teknolojisi bu davranışları Java nesneleri üzerinden yöneterek veritabanına ulaşmadan yormadan halleder.


## Mapped by

```

@Entity
@Table(name="instructor_detail")
public class InstructorDetail{
 ...
 @OneToOne(mappedBy="instructorDetail")
 private Instructor instructor;
 }
 ***********************************************
public class  Instructor{
  ...
 @OneToOne(cascade=CascadeType.ALL)
 @JoinColumn(name="instructor_detail_id")
 private InstructorDetail instructorDetail;
 } ```
 ````
 
 - mappedBy tells Hibernate
    - Look at the instructorDetail property in the Instructor class
    - Use information from the Instructor class @JoinColumn
    - To help find associated instructor


## Fetch Type 

- Aralarında ilişki bulunan Entity sınıflarından bir tarafın yüklenme durumunda diğer tarafın yüklenme stratejisini belirlememizi sağlar. Hibernate de 2 adet fetch type vardır. Bunlar:
- 1-)Eager(Ön Yükleme)
- 2-)Lazy(Tembel/Sonradan Yükleme)

- Eğer @OneToOne ve @ManyToOne ilişkileri kullanıyorsak FetchType olarak Eager kullanmamız daha doğru olur. Yani bir tane Entity nesnesi üzerinden ilişki kurulduğundan ön yükleme yapmak performans açısından sorun oluşturmaz.
- Eğer ki @OneToMany ve @ManyToMany ilişki kullanıyorsak FetchType olarak Lazy kullanmamız daha doğru olur. Yani birden fazla ilişkili nesne olduğundan ön yükleme yapmamız performans açısından kayba neden olur. Bunun için ihtiyaç duyulduğunda yüklemek daha doğru olur.

- Eager will retrieve everything
- Lazy will retrieve on request

- Eager yerine Lazy daha çok tercih ediliyor. Neye ihtiyacımız var ise onu kullanmamız daha mantıklı

![image](https://user-images.githubusercontent.com/61595808/205486450-179c4f09-35c8-4739-8b90-b59e815a553c.png)



## DAO(Data Access Object)

- bir design patterndır.
- It's a design pattern in which a data access object (DAO) is an object that provides an abstract interface to some type of database or other persistence mechanisms.
- ![image](https://user-images.githubusercontent.com/61595808/205486588-1c16c2f9-e55b-4c85-8135-492747b52271.png)
- ![image](https://user-images.githubusercontent.com/61595808/205486595-33d32060-5a54-45b7-a360-13f46be689b5.png)


## HTTP Methods

![image](https://user-images.githubusercontent.com/61595808/205486691-2ccc9d41-0cd4-42ba-8f8f-0b21c2c4b06e.png)

## GET POST

### GET

- Good for debugging
- Bookmark or email URL
- Limitations on data length

### POST

- Can't bookmark(işaretleme) or email URL
- No limitations on data length
- Can also send binary data

#### From load : Call getters
#### From submit : Call setters
#### Save(...) : INSERT new record
#### update(...) : UPDATE existing record

## Application Architecture

Account Controller <---> Account Service <----> Account DAO <----> Database

## Aspect Oriented Programming (AOP)

AspectJ, @Before bu işlemlerde pointcutlar ile * , .. gibilerde package ile işlemlerimizi gerçekleştiriyorunu,yani ulaşıyoruz.
@After Advice, @Around
- ![image](https://user-images.githubusercontent.com/61595808/205487029-5c1c5ae0-f681-4343-b3a7-c8a8ddb3ccc7.png)


## Maven nedir?

- Maven is a Project management tool
- Most populer use of Maven is for build management and dependencies 
- When building your Java project,you may need additional JAR files
        - For example : Spring, Hibernate,Common Logging, JSON etc
- Manually add the JAR files to your build path/classpath


## JAR nedir?

- JAR dosyası, genellikle birçok Java sınıfı dosyasını ve ilişkili meta verileri ve kaynakları dağıtım için tek bir dosyada toplamak için kullanılan bir paket dosya biçimidir. JAR dosyaları, Java'ya özgü bir bildirim dosyası içeren arşiv dosyalarıdır
- JAR stands for Java ARchive. It's a file format based on the popular ZIP file format and is used for aggregating many files into one.









































### Roadmap

![image](https://user-images.githubusercontent.com/61595808/205480956-47c0f466-4ffb-4cc8-8e6f-83c505d6c865.png)











## Layers

![katmannnnn](https://user-images.githubusercontent.com/61595808/204094416-c8ec00bd-bd9f-437d-9f67-2a312168dc76.png)
