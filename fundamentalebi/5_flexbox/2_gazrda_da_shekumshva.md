# გაზრდა და შეკუმშხვა

## შესავალი

ახლა უკეთ გავიგოთ რა მოხდა, როდესაც წინა გაკვეთილში `flex: 1` დავადეთ სტილად.

## გაკვეთილის მიმოხილვა

- ისწავლით `flex`-ის სამ სტილს და როგორ გამოვიყენოთ ისინი.

## flex მოკლედ

`flex`-ის დაწერით სინამდვილეში ვწერთ სამ სტილს შემოკლებით, ანუ ედება სამი სტილი. შემოკლებული სტილები გვაძლევს საშუალებას დავადოთ რამდენიმე მნიშვნელობა ერთად, ისე, რომ ნაკლები წერა დაგვჭირდეს. მაგალითად: 

```css
/* style.css */

h1 {
    margin-top: 5px;
    margin-right: 8px;
    margin-bottom: 10px;
    margin-left: 12px;
}

/* ეს კოდი შემოკლებით იქნება ასე */

h1 {
    margin: 5px 8px 10px 12px;
}
```

ამ შემთხვევაში, `flex` არის შემოკლებული `flex-grow`-ის, `flex-shrink`-ის და `flex-basis`-ის.

```css
/* style.css */

div {
    flex: 1;
}
```

ზედა კოდში, `flex: 1` უდრის: `flex-grow: 1`, `flex-shrink: 1`, `flex-basis: 0`.

ანუ როდესაც `flex: 1`-ს ვადებთ ჩვენს დივს, ის იღებს, როგორც `flex: 1 1 0`.

### Flex-grow

`flex-grow` ელოდება ერთ ციფრს მნიშვნელობად და ეს ციფრი გამოიყენება ფლექს-აითემების "გასაზრდელად".  როდესაც ჩვენ ვადებთ `flex: 1`-ს ყველა დივს, რომელიც ჩვენი კონტეინერის შიგნითაა, ვეუბნებით, რომ ყველა დივი ერთ ზომაზე გაიზარდოს. ამით ყველა დივი ერთი ზომის იქნება. თუ ჩვენ დავამატებთ `flex: 2`-ს მხოლოდ ერთ დივს, ეს დივი სხვა დივებთან შედარებით 2-ჯერ (2x) დიდი იქნება, ვიდრე სხვა დივები.

ამ მაგალითში `flex`-ს აქვს მითითებული `flex-shrink`-ის და `flex-basis`-ის მნიშვნელობები.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="WNmRZMO" data-user="xazy" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/xazy/pen/WNmRZMO">
  flex-grow-example</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

მოცემულ მაგალითში გვაქვს სამი დივი, პირველს და მესამეს აქვს `flex: 1`, ხოლო მეორეს აქვს `flex: 2`. ჯამში გამოდის ოთხი, ანუ იყოფა ოთხ ნაწილად და ნაწილდება ისე, როგორც მითითებულია, ანუ პირველ და მესამე ნაწილს შეხვდებათ ოთხი ნაწილიდან 1-1, ხოლო მეორე დივს შეხვდება ოთხი ნაწილიდან ორი.

### Flex-shrink

`flex-shrink` მსგავსია `flex-grow`-ის, მაგრამ ის ფლექს აითემს "კუმშავს". `flex-shrink` მხოლოდ მაშინ ედება, თუ ყველა ფლექს აითემის ზომა უფრო დიდია, ვიდრე მათი მშობელი კონტეინერი. მაგალითად: თუ ჩვენს 3 დივს ადევს სიგანე: `width: 100px` და `.flex-container` პატარაა `300px`-ზე, ჩვენი დივები შეიკუმშება, რათა ჩაეტიოს ამ კონტეინერში.

`flex-shrink: 1`-ს დროს ყველა ელემენტი თანაბრად იკუმშება, თუ თქვენ არ გსურთ ელემენტის შეკუმშვა, უნდა დაუწეროთ `flex-shrink: 0;`. თქვენ ასევე შეგიძლიათ მაღალი ციფრი გაუწეროთ ზოგიერთ ელემენტს, რათა ნორმალურთან შედარებით უფრო შეიკუმშოს.

აი იხილეთ მაგალითი. გაითვალისწინეთ, რომ ჩვენ შევუცვალეთ `flex-basis` რის მიზეზსაც მალე ავხსნით. თუ თქვენს ბრაუზერს დააპატარავებთ, შეამჩნევთ, რომ `.two` არ შეიკუმშება იმაზე 250 პიქსელზე მეტად, რადგან ასე აქვს გაწერილი, მიუხედავად იმისა, რომ `flex-grow` ეუბნება ყველა ელემენტს ერთნაირი ზომა უნდა ჰქონდეს.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="KKEayxY" data-user="xazy" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/xazy/pen/KKEayxY">
  flex-shrink example</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

როდესაც მიუთითებთ `flex-grow`-ს ან `flex-shrink`-ს, ფლექს აითემები დიდად არ გაითვალისწინებენ თქვენს მიერ გაწერილ `width`-ის მნიშვნელობას. ზედა მაგალითში სამივე დივს ჰქონდა 250 პიქსელი სიგანე, მაგრამ როდესაც მათი მშობელი ელემენტი დიდია, ისინი იზრდებიან, რათა შეავსონ ადგილი. იგივენაირადაა, როცა მშობელი ზედმეტად პატარაა, ისინი შეიკუმშებიან რომ ჩაეტიონ. 

### Flex-basis

`flex-basis` ადებს ფლექს აითემს ზომას, ანუ ნებისმიერი გაზრდა (`flex-grow`) ან შეკუმშვა (`flex-shrink`) დაიწყება იმ ზომიდან, რასაც მივუთითებთ. მისი ჩვეულებრივი მნიშვნელობაა `flex-basis: 0%`. მიზეზი, რის გამოც `auto`-ზე გადავიყვანეთ `flex-shrink`-ის მაგალითზე, იყო ის, რომ, როდესაც `0`-ზე აყენია, ეს აითემები დააიგნორებენ თავიანთ `width`-ს და ყველაფერი თანაბრად შეიკუმშება. `auto`-ს გამოყენებით `flex-basis` ეუბნება აითემს, რომ გაითვალისწინოს ჩვენს მიერ გაწერილი სიგანე (`width: 250px`).

### პრაქტიკაში...

პრაქტიკაში თვენ შესაძლოა საერთოდ არ მოგიწიოთ `flex-grow`, `flex-shrink` ან `flex-basis`-ის გამოყენება. თქვენ უბრალოდ გამოიყენებთ `flex: 1`-ს რათა ყველა დივი თანაბრად გაიზარდოს და `flex-shrink: 0`, რათა ხელი შეუშალოთ ზოგიერთ დივს შეკუმშვაში.