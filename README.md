# AppiumTestAutomation
- Proje Java yazılım geliştirme dili ile Page Object Model'e uygun olarak yazılmış test otomasyon senaryolarını içermektedir.
- Appium frameworkü ile beraber JUnit, Gauge, Log4j, Gson teknolojileri kullanılarak yazılmıştır.
* * HookImp Class
- Appium driverın ayağa kaldırıldığı, ios ve android capabilitylerin tanımlandığı, testin koşacağı urllerin verildiği, ayrıca istenirse uzak bir makinede testlerin koşabileceği şekilde bir hub url tanımlanmış ve hazırlanmıştır.
- BeforeScenario ve AfterSccenario gibi TestNg ve JUnit anatasyonlarıyla senaryolardan ve steplerden önce ve sonra yapılmasını istediğimiz kuralları belirliyoruz. Bunlar driverın ayağa kalkması, gösterilecek loglar, driverin kapatılması gibi işler ve kurallardır.
* - StepImp Class
- Burda test steplerimizi belirliyor ve metodlarımızı oluşturuyoruz. 
- Bu classımızı HookImp classımıza extend ediyoruz çünkü HookImp classındaki anatasyonları ve kuralları buradaki testler koşmadan önce ve koştuktan sonra kullanacağız.
- StepImp classımızda tıklama, yazma, kaydırma ve ihtiyacımız olan bütün fonksiyonlarımızı oluşturuyor ve tanımlıyoruz.
- 
