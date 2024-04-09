# Media Queries

## შესავალი

Media Querie-თი, შესაძლებელია მთლიანი ვებ პროექტის რესტაილინგი, რომელიც მომხმარებლის ეკრანის ზომაზე ერგება. ყველა გაკვეთილი, რომელიც გავიარეთ, ფოკუსირდება ინდივიდუალური ელემენტების მოქნილობაზე, მაგრამ ზოგჯერ გვიწევს რეალური ცვლილებების განხორციელება CSS მნიშვნელობებზე, რათა მოერგონ კონკრეტულ ეკრანის ზომებს. ეს ცვლილებები შესაძლოა იყოს მარჯინის, პადინგის ან ფონტის ზომის ცვლილება და ა.შ. კონკრეტული ცვლილებები დამოკიდებული იქნება თქვენს დიზაინზე, მაგრამ ცვლილება ყველგან ერთნაირად ხდება.

## გაკვეთილის მიმოხილვა

- ისწავლით როგორ გამოიყენოთ მედია ქუერები და გააკეთოთ სრულად რესპონსული საიტი, რომელიც ყველა ეკრანის ზომაზე კარგად გამოიყურება.

## Media query-ს სინტაქსი

მედია ქუერის სინტაქსი ასე გამოიყურება:

```css
body {
  margin: 24px;
}

@media (max-width: 600px) {
  body {
    margin: 8px;
  }
}
```

ზედა მაგალითსი, მარჯინი შეიცვალა ეკრანის ზომის მიხედვით. ყველა ეკრანზე, რომელიც 600 პიქსელს უდრის, ან მასზე პატარაა, მარჯინი ექნება `8px`, და ყველა ეკრანზე, რომელიც `600px`-ია, ამ მაღალი, იქნება `24px`.

სულ ესაა. თქვენ შეგიძლიათ გააკეთოთ ჩახლართული განლაგებები ამ ცოდნით. შეგიძლიათ გააკეთოთ ულიმიტო რაოდენობის მედია ქუერის ერთ დოკუმენტში. დააჭირეთ edit on codepen-ს, რათა შეუცვალოთ ეკრანის ზომები.

<iframe height="300" style="width: 100%;" scrolling="no" title="Media Queries 1 | CSS Responsiveness" src="https://codepen.io/xazy/embed/BaEreEq?default-tab=html%2Cresult&editable=true&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/xazy/pen/BaEreEq">
  Media Queries 1 | CSS Responsiveness</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```css
body {
  background: purple;
}

@media (max-width: 900px) {
  body {
    background: green;
  }
}

@media (max-width: 800px) {
  body {
    background: brown;
  }
}

@media (max-width: 700px) {
  body {
    background: pink;
  }
}

@media (max-width: 600px) {
  body {
    background: blue;
  }
}

@media (max-width: 500px) {
  body {
    background: orange;
  }
}
```

ბრაუზერის პიქსელების მიხედვით, განსხვავებული ფერი ექნება body ელემენტს.

გახსენით ეს CodePen-იც და შეუცვალეთ ზომები, ასევე კარგად დააკვირდით კოდს. აქ main თეგს 800 პიქსელზე და ქვევით ხდება column. ჰედერს ედება პადინგი 24 პიქსელი და ცენტრში ექცევა ტექსტი და ა.შ.

```css
@media (max-width: 800px) {
  main {
    flex-direction: column;
  }
  header {
    text-align: center;
    padding: 24px
  }
  aside {
    width: auto;
  }
  ul {
    display: flex;
    gap: 16px;
    justify-content: center;
    padding: 0;
  }
}
```

<iframe height="300" style="width: 100%;" scrolling="no" title="Media Queries 2 | CSS Responsiveness" src="https://codepen.io/xazy/embed/VwNXOOM?default-tab=html%2Cresult&editable=true&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/xazy/pen/VwNXOOM">
  Media Queries 2 | CSS Responsiveness</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## რჩევები

### სხვა queries

ყველა ზედა მაგალითში, ჩვენს queries აქვს სპეციფიური `max-width`, რომელიც ადებს სტილებს უველა ეკრანის რეზოლუციას, მიცემულ ზომაზე ქვემოთ. სხვაგვარად რომ ვთქვათ: `max-width` ქუერიში დაადებს სტილს `max-width`-ით განსაზღვრულ ზომამდე. ასევე შეგვიძლია განვსაზღვროთ `min-width`, რომელიც დაედება ეკრანებს, რომლებიც დიდია გადაცემულ მნიშვნელობაზე. ასევე შეიძლება `max-height` და `min-height`-ის გამოყენებაც.

### ლიმიტირებული მედია ქუერის

როგორც ვახსენეთ, შესაძლებელია ულიმიტო რაოდენობის მედია ქუერის გაკეთება ყველა შესაძლო ეკრანის ზომისთვის. მაგრამ, საუკეთესო პრაქტიკაა შევამციროთ მისი გამოყენება და დამოკიდებულნი ვიყოთ ბუნებრივ მოქნილობაზე. ნახეთ ზედა მაგალითი "ჩემი საიტი". მას დასჭირდა მხოლოდ ერთი მედია ქუერი რათა მოერგოს ყველა დესკტოპ და მობილურ ზომას და არ საჭიროებს მეტის შექმნას.

### ხშირი ეკრანის ზომები (breakpoints)

"Breakpoint" არის ტერმინი, რომელიც ეკრანის ზომებისთვის გამოიყენება და ამოქმედებს მედია ქუერის. თქვენ ბევრ ვარიანტს შეხვდებთ, თუ რამდენი და რა ზომის ბრეაქფოინთები უნდა გქონდეთ. ყველაზე ხშირი ბრექიფოინთებია `320px`, `480px`, `768px`, `1024px` და `1200px`. რაც უფრო ცოტა წერტილს გამოიყენებთ უკეთესია. მობილური ტელეფონები ძირითადად 500 პიქსელზე ქვემოთ არიან. ტაბლეტები 500 დან 1000 პიქსელამდე. ყველაფერი, 1000 პიქსელის ზემოთ ჩვეულებრივი დესკტოპის/ლეპტოპის ზომაა. 

ეს არ ნიშნავს, რომ თქვენი პროექტი თითოეულ მედია ქუერისზე ააწყოთ, ყველა მოწყობილობისთვის. თითოეულ პროექტს ექნება განსხვავებული მოთხოვნები, დიზაინის მიხედვით. როგორც ზემოთ ავღნიშნეთ, სცადეთ ბრეიქფოინთების ლიმიტირება და მხოლოდ როდესაც საჭიროა და ელემენტი არ ეტევა, მაშინ გამოიყენეთ.

### გადიდება

ყველა ბრაუზერს აქვს გვერდის გადიდების ფუნქცია (zoom), რომელიც ცვლის რეზოლუციას ამ გვერდზე. თუ თქვენი ბრაუზერი ზუსტად `1000px` სიგანისაა, გვერდის გადიდება ეკრანს "დააპატარავებს" და მედია ქუერის აამოქმედებს განსაზღვრულ რეზოლუციაზე. გამოზუმვა, ანუ დაპატარავება, შესაძლოა მოსახერხებელი იყოს პრობლემების მოსაძებნად, რაც განიერ ეკრანებზე შეიძლება შეგვხვდეს.

## Print სტილები

მედია ქუერის გამოყენებისას ხშირად შეხვდებით `screen` სიტყვას:

```css
@media screen and (max-width: 480px) {
}
```

`sreen` არ არის აუცილებელი, მაგრამ ერთ საჭირო ფუნქციას გვაძლევს: ცვლის სტილებს მედიას ტიპის მიხედვით. ყველაფერი, რაც გავიარეთ, მიმართული იყო სტილების რაღაც ზომაზე სანახავად, ამიტომ `screen` საჭირო არ იყო. ახლა ვისწავლოთ როგორ დავადოთ სტილი, როდესაც გვერდის ამოპრინტერება გვინდა. ამისთვის ვიყენებთ `print` სიტყვას.

```css
@media print {
  /* პრინტერისთვის განკუთვნილი სტილები */
}
```

ეს შეგიძლიათ არ გაითვალისწინოთ, მაგრამ მაინც უნდა იცოდეთ. თუ ამ პროექტის მსგავს საგანმანათლებლო პროექტს გააკეთებთ, ან ბლოგს საჭირო ფუნქციაა. შეგიძლიათ ამ გვერდზე დააჭიროთ <kbd>Ctrl</kbd> + <kbd>P</kbd> და ნახოთ როგორაა შეცვლილი დიზაინი პრინტერისთვის.

ამ დროს ხშირია ტექსტის შავ-თეთრში გადაყვანა და `display:none`-ს დადება გამოუსადეგარ სექციებზე, მაგალითად ნავიგაციაზე.

## დავალება

<div className="homework">

1. გადახედეთ [მედია ქუერის გამოყენებას MDN-ზე](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries). არსებობს კიდევ რაღაცეები, რისი ცოდნაც კარგი იქნება, მაგრამ იშვიათადაა გამოყენებული.

</div>

## დამატებითი რესურსები

- [მედია ქუერის გაკვეთილი](https://www.freecodecamp.org/news/css-media-queries-breakpoints-media-types-standard-resolutions-and-more/) FreeCodeCap-ზე, განიხილავენ იგივეს, რაც აქ განვიხილეთ.
- თუ გსურთ პრაქტიკული [რესპონსიული განლაგების კურსი](https://courses.kevinpowell.co/conquering-responsive-layouts), ეს კარგი ვარიანტია, უბრალოდ უნდა დარეგისტრირდეთ.