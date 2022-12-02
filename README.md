# Spring-Boot-Turkish-Notes


## Spring Nedir?

- Spring popüler bir Java frameworküdür.

## Tomcat Nedir?

- Web sunucusudur.

## IoC(Inversion of Control)

- Bir yazılım tasarım prensibidir

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

<form action=" ....." karşılık gelen kısımdır.
     <form action=" ....."  method="GET"> ---  </form>

## @RequestParam()

- Attribute ismini yazarız
  
  
