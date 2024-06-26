# HTML და CSS ინსპექტირება

## შესავალი

კოდის ინსპექტირების ცოდნა ფრონტენდის ერთ-ერთი მნიშვნელოვანია. ამ გაკვეთილში გავივლით Chrome Dev Tools-ს, რომელიც დაგვეხმარება დეტალური ინფორმაცია გავიგოთ ჩვენს ელემენტებსა და CSS სტილებზე, ასევე ის დაგვეხმარება პრობლემების პოვნასა და მოგვარებაში ჩვენს კოდში.


## გაკვეთილის მიმოხილვა

- ისწავლით როგორ გამოიყენოთ ელემენტის ინსპექტორი.
- ისწავლით როგორ აირჩიოთ და დააინსპექტიროთ კონკრეტული ელემენტი.
- ისწავლით როგორ დავტესტოთ HTML და CSS ინსპექტორში.


## ინსპექტორი

ინსპექტორის გასახხსნელად, თქვენ შეგიძლიათ დააწვეთ მაუსის მარჯვენა ღილაკს ვებსაიტის ნებისმიერ ელემენტზე და აირჩიოთ `inspect` ან დააწვეთ კლავიატურაზე <kbd>F12</kbd>. ახლა თავად სცადეთ ეს და არ შეშინდეთ თუ ბევრ რამეს დაინახავთ.


## ელემენტების ინსპექტირება

ელემენტების გამყოფილებაში თქვენ დაინახავთ მთლიან HTML-ს სტრუქტურას, რაც ამ გვერდზეა. შეგიძლიათ დააწვეთ ნებისმიერ ელემენტს ამ სტრუქტურაში და აირევთ მას. 

![inspeqti](https://raw.githubusercontent.com/XazyProject/masala/main/fundamentalebi/4_css_fundamentalebi/html_da_css_inspeqtireba-imgs/01.png)

როდესაც ელემენტი მონიშნულია, Styles ტაბი, რომელიც მარჯვენა მხარესაა, გვაჩვენებს ყველა ამ ელემენტის სტილს, ასევე სტილებს, რომლებიც სხვა სტილმა გადააწერა ზევიდან (გადახაზული ელემენტები). მაგალითად:

![stilebi](https://raw.githubusercontent.com/XazyProject/masala/main/fundamentalebi/4_css_fundamentalebi/html_da_css_inspeqtireba-imgs/02.png)


## სტილების გატესტვა ინსპექტორში

სტლების სექციაში შეგიძლიათ დაარედაქტიროთ სტილები თავად ბრაუზერშივე. დააწექით ნებისმიერ HTML ელემენტს, რომლის სტილების ნახვაც გინდათ, შემდეგ სტილების სექციაში ჩამოთვილი დადებული სტილებიდან დააწექით ნებისმიერ მნიშვნელობას და გადააკეთეთ ის. ასევე შეგიძლიათ დაამატოთ თქვენი სტილი. ყველაფერი რასაც შეცვლით და დაამატებთ რეალურ დროში შეიცვლება ბრაუზერში, მაგრამ გვერდის დარეფრეშებისთანავე ისევ ძველ კოდს დაუბრუნდება. ეს ცვლილება არანაირ გავლენას არ ახდენს ორიგინალ კოდზე, რომელიც თქვენს ტექსტის ედიტორში გაქვთ, მაგრამ ეს აუცილებელი და საჭირო ფუნქციაა სწრაფად დასატესტად ან პრობლემების მოსაძებნად, ამიტომ ხშირად მოგიწევთ ამის გამოყენება.


## დავალება

<div className="homework">

- გახსენით ინსპექტი ამ გვერდზე, მონიშნეთ სხვადასხვა ელემენტები და შეუცვალეთ ფონი, ფერი, ფონტის ზომა და ა.შ.


- ქვემოთ მოცემულ სიას შეუცვალეთ ის, რასაც თავად გეუბნებათ.
<ol>
    <li className="pirveli">დამადე წითელი ფერი</li>
    <li className="meore">გამიზარდე ფონტის ზომა</li>
    <li className="mesame">ფონი მინდა შავი და ფერი ყვითელი</li>
</ol>

</div>