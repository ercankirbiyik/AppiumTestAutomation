# AppiumTestAutomation
- Proje Java yazılım geliştirme dili ile Page Object Model'e uygun olarak yazılmış test otomasyon senaryolarını içermektedir.
- Appium frameworkü ile beraber JUnit, Gauge, Log4j, Gson teknolojileri kullanılarak yazılmıştır.
* * HookImp Class
- Appium driverın ayağa kaldırıldığı, ios ve android capabilitylerin tanımlandığı, testin koşacağı urllerin verildiği, ayrıca istenirse uzak bir makinede testlerin koşabileceği şekilde bir hub url tanımlanmış ve hazırlanmıştır.
- BeforeScenario ve AfterSccenario gibi TestNg ve JUnit anatasyonlarıyla senaryolardan ve steplerden önce ve sonra yapılmasını istediğimiz kuralları belirliyoruz. Bunlar driverın ayağa kalkması, gösterilecek loglar, driverin kapatılması gibi işler ve kurallardır.
* * StepImp Class
- Burda test steplerimizi belirliyor ve metodlarımızı oluşturuyoruz. 
- Bu classımızı HookImp classımıza extend ediyoruz çünkü HookImp classındaki anatasyonları ve kuralları buradaki testler koşmadan önce ve koştuktan sonra kullanacağız.
- StepImp classımızda tıklama, yazma, kaydırma ve ihtiyacımız olan bütün fonksiyonlarımızı oluşturuyor ve tanımlıyoruz.
* * Selector Interface
* Selector Interfaceimizde android ve iosta ortak olarak kullanacağımız fonksiyonları ve fonksiyonların içinde kullanacağı elementleri çağırma işlemlerini yapıyoruz. 
* Oluşturduğumuz Selector Interfaceimizi HookImp classımızda newleyip kullanıyoruz.
* * AndroidSelector Class
* AndroidSelector classımızda android cihazlarda kullanacağımız locater tiplerini tanımlıyoruz.
* Bu classımızı Selector Interfaceimize implemente ediyoruz ve oradan gelecek olan fonksiyonları kullanabilmek ve özelleştirebilmek adına Override ediyoruz.
* * IOSSelector Class
* IOSSelector classımızda ios cihazlarda kullanacağımız locater tiplerini tanımlıyoruz.
* Bu classımızı Selector Interfaceimize implemente ediyoruz ve oradan gelecek olan fonksiyonları kullanabilmek ve özelleştirebilmek adına Override ediyoruz.
* * SelectorType Class
* SelectorType classımızda cihaz tiplerimizi android ve ios olarak tanımlıyoruz.
* * SelectorFactory Class
* SelectorFactory classımızda selector tiplerimizi android ve ios olarak tanımlıyoruz ve bunları IOS ve Android Selector claslarımıza bağlıyoruz.
* * SelectorInfo Class
* SelectorInfo classımızda kullanacağımız selector tiplerinin detaylarını belirtiyoruz ve bu detayları Selector interfaceimizde çağırarak kullanıyoruz.
* * ElementInfo Class 
* ElementInfo classımızda projemizde kullanacağımız locatorların tiplerini genel hatlarıyla veriyoruz.
* Bu locatorları android ve ios olarak ayrı ayrı tutacağımızı bu classımızda belirtiyoruz.
* * StoreHelper enum
* StoreHelper enumımızda Gson kütüphanesi kullanarak tutacağımız elementlerimizin pathini veriyoruz.
* Bu classta ayrıca locatorların bulunduğu pathleri listelere çekiyoruz ve rahat kullanım sağlıyoruz.
* * RandomString Class
* Bu classımızda ihtiyaç halinde kullanılabilecek random kelime, numara, alphanumeric ihtiyaçlarımızı karşılayacak bazı fonksiyonlar hazırlanmıştır.
* Bu fonksiyonları RandomString Classımızı StepImp Classımızda çağırarak kullanabiliriz.
* * Faladdin.spec
* Bu spec dosyamızda StepImp Classımızda oluşturduğumuz steplerimizi Gauge kullanarak çağırıyoruz ve anlaşılır bir dil ile testlerimizi oluşturup koşuyoruz.
* Testlerimizi runladığımız dosyamız burasıdır.
* * Faladdin.cpt
* Consept dosyalarımız yine Gauge dili ile daha anlaşılır ve takibi kolay testler oluşturmamızı sağlayan dosyalarımızdır.
* Spec dosyalarımızda çağırdığımız ve birden çok stepten oluşan satırlarımızı burada tutmaktayız.
* * element-values Faladdin.json
* Bu json dosyalarımızda locaterlarımızı spesifik bir isimle ve tiple tutup android ve ios için ayrı ayrı çağırabileceğimiz elementler halinde tutuyoruz.
