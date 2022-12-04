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


## Tomcat Nedir?

- Web sunucusudur.

## IoC(Inversion of Control)

- Bir yazılım tasarım prensibidir.
-  Ioc ile Uygulama içerisindeki obje instance’larının yönetimi sağlanarak, bağımlılıklarını en aza indirgemek amaçlanmaktadır.
- Yazdığımız kod bloğu çalışacağı zaman, framework bizim kodumuzu çağırır ve çalıştırır daha sonra kontrol yeniden framework’e geçmesi olayının tümüne Inversion Of Control adı verilmektedir.

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





























## Layers

![katmannnnn](https://user-images.githubusercontent.com/61595808/204094416-c8ec00bd-bd9f-437d-9f67-2a312168dc76.png)
