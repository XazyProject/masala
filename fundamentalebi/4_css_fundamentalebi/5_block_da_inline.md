# შესავალი

წინა გაკვეთილში ვისწავლეთ ბოქს მოდელი, ახლა ჩვენ შეგვიძლია მისი მოდიფიკაცია `display` სტილის შეცვლით. CSS-ს აქვს ბოქსის ორი ტიპი: `block` და `inline` ბოქსები, რომლებიც განსაზღვრავენ ელემენტის "საქციელს". `display` სტილი მართავს, თუ როგორ გამოჩნდებიან HTML ელემენტები გვერდზე. ჩვენ განვიხილავთ მის სხვადასხვა ოფიცებს.

# გაკვეთილის მიმოხილვა

- თქვენ ისწავლით განსხვავებას `block` და `inline` ელემენტების შესახებ.
- თქვენ ისწავლით რომელი ელემენტებია თავიდანვე `block` და რომელი `inline`.
- თქვენ ისწავლით `div`-ის და `span`-ის შესახებ.

# Block vs Inline

ელემენტების უმეტესობა, რომლებიც ისწავლეთ, თითქმის ყველა block ელემენტია. სხვა სიტყვებით რომ ვთქვათ, მათ ადევთ სტილი `display: block;` ჩვეულებრივ, ელემენტები ვებგვერდზე გამოჩნდება ერთმანეთის თავზე დალაგებული, თითოეული ელემენტი იწყება ახალ ხაზზე.

Inline ელემენტები, არ იწყებენ ახალ ხაზზე. ისინი ჩნდებიან იმ ელემენტის გვერძე, რომლის შემდეგაც დავწერთ ამ ელემენტს. ამის მაგალითია ლინკი, ანუ `<a>` თეგი. თუ თქვენ ლინკის თეგს პარაგრაფის შუაში ჩასვავთ, ის ისე იქნება, თითქოს პარაგრაფის ნაწილია. ([მაგალითად ასე...](https://youtu.be/pqqAfFmPUr8)) ლინკის თეგი მოთავსდება პარაგრაფის სხვა სიტყვებთან ერთად. 

Inline ელემენტებია: `<a>`, `<b>`, `<i>`, `<img>` `<input>` და ა.შ.

Block ელემენტებია: `<div>`, `<h1> - <h6>`, `<li>`, `<ol>`, `<p>` და ა.შ.

### Inline-block ელემენტები

Inline-block ელემენტები ისე იქცევიან, როგორც უბრალოდ inline ელემენტები, მაგრამ უბრალოდ inline-ზე ზევით და ქვევით მარჯინს/პადინგს ვერ დავამატებთ, ასევე შეგვიძლია გავუწეროთ სიმაღლე და სიგანე, ვიდრე უბრალოდ inline. `display: inline-block`-ის ცოდნა არის მნიშვნელოვანი, რომელსაც პრაქტიკაში უკეთ გაიგებთ.

### None

`none` არის display-ს ერთ-ერთი მნიშვნელობა. `display: none;`-ს დადების დროს ეს ელემენტი აღარ გამოჩნდება საიტზე, არც ადგილს დაიკავებს, ის უბრალოდ სიცარიელეში დაიკარგება.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="gOELVvJ" data-user="xazy" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/xazy/pen/gOELVvJ">
  inline-block-inline-block</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

# Div და span

შეუძლებელია ვისაუბროთ ბლოკ და ინლაინ ელემენტებზე და არ ვახსენოთ `div` და `span` ელემენტები. ყველა ელემენტი, რომელიც ვისწავლეთ, აძლევს მათში მოთავსებულ ტექსტს რაიმე მნიშვნელობას, სტილს. მაგალითად პარაგრაფის ელემენტი ეუბნება ბრაუზერს, რომ ეს ტექსტი გამოაჩინოს, როგორც პარაგრაფი. `<strong>` ელემენტი ეუბნება, რომ მათ შორის მყოფი ტექსტი მნიშვნელოვანია და მუქად აჩვენებს, ხოლო `div` და `span` ელემენტები არანაირ მნიშვნელობას არ აძლევს მათში მოთავსებულ კონტენტს. ისინი უბრალოდ ყუთები არიან, რომლებიც არაფერს არ შეიცავენ.

ასეთი ელემენტების არსებობა უფრო გამოსადეგარია, ვიდრე ერთი შეხედვით ჩანს. მათ შეგვიძლია მივცეთ ID ან კლასი და გავსტილოთ CSS-ში. ეს მათი ძირითადი დანიშნულებაა. ასევე იყენებენ სხვა ელემენტების დასაჯგუფებლად, ამით უკეთესად შეიძლება მათი პოზიციონირება ვებგვერდზე. 

თქვენ შეიძლება შექმნათ `<div>` ელემენტი, რომელშიც მოთავსებული იქნება ყველა ელემენტი, რომელიც თქვენი ვებგვერდის თავშია (ლოგო და ნავიგაცია).

div ბლოკ ელემენტია, მაგრამ ასეთი ელემენტების ინლაინად გადაქცევა თუ დაგვჭირდა, უკვე ვიცით როგორც.

div-ით ასევე ადვილია საიტი დავყოთ სექციებად, რომლის მართვაც უფრო მარტივი იქნება და ასევე კოდის წაკითხვაც გამარტივდება.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="OJqbKqP" data-user="xazy" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/xazy/pen/OJqbKqP">
  divs</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

`<span>` არის inline თეგი, რომელიც ტექსტის რაიმე ნაწილის გამოსაყოფად და მის გასასტილად გამოიყენება. `<span>` ელემენტი მსგავსია `<div>` ელემენტის, მაგრამ ეს ინლაინია, ხოლო დივი ბლოკი.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="NWJdWKY" data-user="xazy" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/xazy/pen/NWJdWKY">
  inline</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

წინა გაკვეთილში ვისწავლეთ margin და padding. იმისათვის, რომ რაიმე ელემენტი, მაგალითად div ვებგვერდის ცენტრში დავაყენოთ, შეგვიძლია გამოვიყენოთ margin. როგორც დავინახეთ div მთლიანი საიტის სიგანეზე ჯდება, ხოლო თუ მას რაიმე სიგანეს, ანუ `width`-ს მივანიჭებთ და მოგვინდება მისი ცენტრში მოთავსება, ვუწერთ ასე:

```css
/* style.css */

div {
    margin: 0 auto;
}
```

ეს ზევით-ქვევით დაადებს მარჯინს 0 პიქსელს, ხოლო გვერდებზე ზუსტად თანაბრად, რის საშუალებასაც ადგილი მისცემს და ზუსტად ცენტრში იქნება. ეს არ მუშაობს პადინგზე.

# დავალება

<div className="homework"> 

1. გადადით [ჩვენს CSS დავალებების რეპოზიტორში](https://github.com/XazyProject/css-davalebebi) და შედით `margin-da-padding` საქაღალდეში. გაეცანით თითოეულ README ფაილს და გააკეთეთ დავალებები ამ თანმიმდევრობით: 
    - 01-margin-da-padding-1
    - 02-margin-da-padding-2

    შენიშვნა: თითოეულის ამოხსნა შეგიძლიათ ნახოთ `amoxsna` ფონდელრში.

2. გამოიყენეთ ყველაფერი, რაც ისწავლეთ, რათა გააუმჯობესოთ თქვენი რეცეპტების საიტი. ახლა უბრალოდ სია გაქვთ და სცადეთ გააფორმოთ ფერებით, ფონტის ზომებით, მარჯინით, პადინგით და ა.შ.

</div>