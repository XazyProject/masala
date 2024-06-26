# HTML და CSS შესავალი

## შესვალი

დადგა დრო, რომ დავიწყოთ უკვე „რაღაცეების“ კეთება. ამ სექციაში ვისწავლით HTML & CSS-ის ფუნდამენტალებს.

## HTML და CSS

HTML და CSS არის ორი ენა, რომლებიც ერთმანეთად მუშაობენ და ქმნიან ყველაფერს, რასაც ინტერნეტში ვხედავთ. HTML არის ჩონჩხი, რომელზეც საიტია დაშენებული, ხოლო CSS ადებს სტილს, ანუ ალამაზებს გამოყენებულ ელემენტებს. ანუ HTML დებს ინფორმაციას საიტზე, ხოლო CSS აძლევს პოზიციას, ფერს, ფონტს და ალამაზებს.


HTML და CSS-ს ხშირად მოიხსენებენ პროგრამულ ენებად, მაგრამ ეს ასე არ არის, რადგან ისინი მხოლოდ „ინფორმაციის პრეზენტაციისთვის“ გამოიყენება და არ შეუძლია რაიმე ლოგიკის დაპროგრამება. პროგრამირების ენა არის JavaScript, რომელსაც მოგვიანებით ვისწავლით, ჯავასკრიპტს შეუძლია „რაღაცეების“ გაკეთება და ჩვენი გაწერილი ლოგიკით მუშაობა.

ჯავასკრიპტსა და HTML-CSS-ს შორის განსხვავება შეგიძლიათ ნახოთ [ამ სტატიაზე](https://brytdesigns.com/html-css-javascript-whats-the-difference) 


## ელემენტები და თეგები

თითქმის ყველა ელემენტი HTML გვერდზე არის კონტენტი, რომელიც შემორტყმულია გამხსნელი და დამკეტი თეგებით.

გამხსნელი თეგები ეუბნება ბრაუზერს, რომ ეს არის HTML ელემენტის დასაწყისი. მაგალითად ასე გამოიყურება პარაგრაფის თეგი: `<p>`

დამკეტი თეგი ეუბნება ბრაუზერს სად მთავრდება ელემენტი, ეს თითქმის იგივეა, როგორიც გამხსნელი თგია, მაგრამ მას წინ დახრილი ხაზი აქვს და პარაგრაფის დამკეტი თაგი გამოიყურება ასე: `</p>` 

მათ შორის, როგორც უკვე ვახსენეთ კონტენტია, რაც საიტზე გამოჩნდება:

```html
<p> ეს არის პარაგრაფი </p>
```

### უფრო დეტალურად:

- `<p>` არის გამხსნელი თეგი
- “ეს არის პარაგრაფი“ არის კონტენტი, რომელიც შემოსაზღვრულია გამხსნელი და დამკეთი თეგებით.
-  `</p>` არის დამკეთი თეგი.

თქვენ შეგიძლიათ წარმოიდგინოთ ელემენტები, როგორც კონტეინერები, რომლებშიც კონტენტი აწყვია. გამხსნელი და დამკეტი თეგები ეუბნებიან ბრაუზერს რა კონტენტს შეიცავს ელემენტი. ბრაუზერს შეუძლია გამოიყენოს ეს ინფორმაცია, რათა განსაზღვროს როგორ გადმოცეს და დააფორმატოს კონტენტი.

მაგრამ არსებობს ელემენტები, რომლებასც არ აქვთ დამკეთი თეგები, მაგალითად: `<br />` ან `<img />`. მათი გამოყენება დახრილი ხაზის გარეშეც შეიძლება, როგორც `<br>` და `<img>`. სხვა თვით-დახურვად ელემენტებს და მათ განმარტებებს მოგვიანებით ვისწავლით.

## HTML ელემენტები

არსებობს 100-ზე მეტი HTML ელემენტი. ესენია ყველაზე გამოყენებადი:

`h1`, `h2`, `h3`, `h4`, `h5`, `h6`, `img`, `div`, `a`, `li`, `ul`, `ol`, `head`, `body`, `main`, `nav`, `form`, `table`, `input`, `table`, `video`, `span`, `b`, `i`.

შემდეგი გაკვეთილებიდან დავიწყებთ თითოეულის განხილვას.

