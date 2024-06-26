# Box Model

## შესავალი

ახლა, როდესაც უკვე იცი  HTML და CSS-ს სინტაქსი, გადავდივართ უფრო სერიოზულ თემაზე. ყველაზე მნიშვნელოვანი CSS-ში ელმენტების სწორად განლაგების ცოდნაა. ფონტის ზომისა და ფერების შცვლაც მნიშვნელოვანია, მაგრამ ელემენტების იქ განთავსება, სადაც თქვენ გსურთ უფრო საჭიროა.

იმის სწავლა, როგორ განვალაგოთ სწორად ელემენტები ვებგვერდზე არც ისე რთულია, როდესაც უკვე კარგად გაიაზრებთ ძირითად "აზრს". სამწუხაროდ, ბევრ მოსწავლეს ეჩქარება HTML-სა და CSS-ს სწრაფად სწავლა, რათა მალე გადავიდნენ JavaScript-ზე და ტოვებენ ამ ფუნდამენტალურ საკითხებს. 

## გაკვეთილის მიმოხილვა

- თქვენ ისწავლით *box model*-ის შესახებ.
- თქვენ ისწავლით, როგორ მიანიჭოთ ელემენტებს ზუსტი ზომა `margin`, `padding` da `border`-ის გამოყენებით.


## The Box Model

ყველაფერი საიტზე არის ყუთებში მოქცეული. ამ ყუთებს აქვთ თავიანთი თანმიმდევრობა და შესაძლოა ეს ყუთები ერთმანეთის შიგნით, გვერდიგვერდ, ზევით და ქვევით იყვნენ. რომ გქონდეთ წარმოდგენა ეს როგორ მუშაობს, შეგიძლიათ დაადოთ თქვენს საიტზე ყველა ელემენტს წითელი ყუტი, რათა მიხვდეთ კარგად:

```css
/* styles.css */
* {
  border: 2px solid red;
}

/* ამით ყველაფერს დაედება წითელი საზღვრები. */
```

![boxmodel](https://raw.githubusercontent.com/XazyProject/masala/main/fundamentalebi/4_css_fundamentalebi/box_model-imgs/00.png)

ეს შეგიძლიათ სცადოთ ნებისმიერ საიტზე და ნახავთ რამდენი ბოქსია გამოყენებული.

![site-example](https://raw.githubusercontent.com/XazyProject/masala/main/fundamentalebi/4_css_fundamentalebi/box_model-imgs/01.png)

ამ ყუთების ზომის მანიპულაცია ბევრნაირად შეიძლება, რომლებსაც აუცილებლად ვისწავლით, ამ გაკვეთილში კი შევეხებით მათ შორის დაშორებებს, `padding`, `margin` და `border`-ის დახმარებით.

![marginpaddingborder](https://raw.githubusercontent.com/XazyProject/masala/main/fundamentalebi/4_css_fundamentalebi/box_model-imgs/02.png)

- `padding` ზრდის სივრცეს ამ ყუთის საზღვრიდან, ანუ ჩარჩოდან, ამ ყუთში არსებულ კონტენტამდე, იქნება ეს ტექსტი, ფოტო თუ ა.შ. წარმოიდგინეთ გაქვთ ნახატი ჩარჩოში, რათქმაუნდა თქვენ არ გინდათ ამ ნახატს მოკიდოთ ხელი და თქვენ აკეთებთ დაშორებას ჩარჩოდან ნახატამდე, სწორედ ეს სივრცეა `padding`.

- `margin` ზრდის სივრცეს ამ ყუთის საზღვრიდან, ანუ ჩარჩოდან გარეთ მყოფ სხვა ყუთებამდე, ანუ თუ ერთმანეთის ორი ყუთი დგას და ერთ-ერთს დავუწერთ `margin`-ს, მათ შორის გაიზრდება სივრცე. უკეთესად გასაგებად წარმოიდგინეთ ნახატი, რომელიც კედელზე ჰკიდია. დაშორება ამ ნახატის ჩარჩოდან უახლოეს ავეჯამდე, ან სხვა ნახატამდე არის `margin`.

- `border` ზრდის სივრცეს მარჯინსა და პადინგს შორის. თუ თქვენ დახატავთ ხაზს ნახატის გარშემო, ეს არის ბორდერი, ანუ საზღვარი, შიგნითა და გარე სივრცეს შორის.


ამ სტილების გამოყენება შემდეგნაირად შეგვიძლია:

```css
p {
    margin: 5px;
    padding: 5px;
}
```

აქ მარჯინიც და პადინგიც პარაგრაფის ელემენტს დაედება ოთხივე მხარეს, მაგრამ შეგვიძლია გავაკეთოთ ისე, რომ რომელ მხარესაც გვინდა იქით დავადოთ.


```css
p {
    margin: 5px 10px 8px 3px;
}
/* პირველი მნიშვნელობა ადებს ზევით ზომას */
/* მეორე მნიშვნელობა ადებს მარჯვნივ ზომას */
/* მესამე მნიშვნელობა ადებს ქვევით ზომას */
/* მეოთხე მნიშვნელობა ადებს მარცხნივ ზომას */
/*         5px            */
/*      -----------       */
/*      |         |       */
/* 3px  |         |  10px */
/*      |         |       */
/*      -----------       */
/*          8px           */
```

ზედა მაგალითში განვიხილეთ, როდესაც ოთხივე მხარეს სხვადასხვა ზომას ვადებთ, ხოლო თუ ზევით-ქვევით ერთნაირი და მარცხნივ-მარჯვნივ ერთნაირი ზომები გვინდა, მაშინ ორ მნიშვნელობას დავუწერთ 4-ის ნაცვლად, პირველი ზედა-ქვედას განსაზღვრავს, მეორე - მარცხენა-მარჯვენას.

```css
h1 {
    padding: 0 10px;
}
```

ამ მაგალითში h1 ელემენტს პადინგი ზევით-ქვევით 0 პიქსელი ექნება (გაითვალისწინეთ, როდესაც 0 პიქსელი გინდათ `px`-ს აღარ უწერთ.), ხოლო მარცხნივ და მარჯვნივ 10-10 პიქსელები.

რაც შეეხება ბორდერს, ანუ საზღვარს. მას შეუძლია მიიღოს სხვადასხვანაირი მნიშვნელობები.

```css
p {
    border: 1px solid #ccc;
}
```

პირველი მნიშვნელობა არის ზომა, რა ზომაც გვინდა იყოს ეს საზღვარი, `solid` არის როგორი იყოს საზღვარი, ამ შემთხვევაში უბრალოდ ხაზი იქნება, შეგვიძლია სხვადასხვა სახის საზღვარი გვქონდეს, მაგალითად `dotted`, რომელიც საზღვარს წერტილებად აქცევს, `dashed`, რომელიც ხაზებად აქცევს და ა.შ. სარული სიის სანახავად ნახეთ [w3shools-ის სია.](https://www.w3schools.com/css/css_border.asp)

<div className='homework'>

- შექმენით ფაილი, რომელშიც გექნებათ სამი ელემენტი, სათაური, პარაგრაფი და მეორე პარაგრაფი. მეორე პარაგრაფში შექმენით სია. მათში ჩაწერეთ რაიმე ტექსტი.

- პარაგრაფებს დაადეთ სხვადასხვა კლასები, რათა CSS ფაილში შეძლოთ გასტილვა.

- უნივერსალური სელექტორის (`*`) გამოყენებით ყველაფერს დაადეთ წითელი ბორდერი ასე:
```css
* {
  border: 2px solid red;
}
```
- სათაურის ელემენტს დაადეთ მარჯინი ქვედა მხარეს - 10 პიქსელი, პირველ პარაგრაფს დაადეთ პადინგი ყველა მხრიდან 15 პიქსელი, მეორე პარაგრაფს დაადეთ პადინგი 10 პიქსელი, ზედა მარჯინი 20 პიქსელი, ხოლო მასში მყოფ სიას დაადეთ 10 პიქსელი პადინგი, `<li>` თეგს კი ზედა მარჯინი 2 პიქსელი, მარჯვენა - 10 პიქსელი, ქვედა - 15 პიქსელი, მარცხენა - 5 პიქსელი. 


</div>