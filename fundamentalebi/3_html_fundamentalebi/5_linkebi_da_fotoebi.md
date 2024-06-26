# ლინკები და ფოტოები

## შესავალი

ლინკი არის ერთ-ერთი ყველაზე მნიშვნელოვანი HTML-ს თეგი, ეს გვაძლევს საშუალებას დავუკავშიროთ ერთმანეთთან HTML გვერდები ინტერნეტში.

ამ გაკვეთილში ვისწავლით როგორ გავაკეთოთ ლინკები, რომლებიც სხვა ვებსაიტებს დაუკავშირდებიან და ვისწავლით სურათის ჩასმას გვერდზე.

## მომზადება

იმისათვის, რომ ვივარჯიშოთ ამ თემებზე, შევქმნათ HTML პროექტი.

1. შექმენით ახალი ფოლდერი, სახელად `link-and-image`.
2. ამ ფოლდერში შექმენით ახალი ფაილი და დაარქვით `index.html`.
3. გახსენით ეს ფაილი VSCode-ში და დაწერეთ HTML ჩონჩხი.
4. ახლა დაამატეთ h1 საიტზე:


```html
<h1>მთავარი გვერდი</h1>
```

## Anchor ელემენტი

Anchor ელემენტი, ანუ `<a>`, გამოიყენება HTML-ში ლინკის შესაქმნელად. ლინკის გამოსაყენებლად საჭიროა ეს ელემენტი ტექსტის ნაწილს ან სხვა ელემენტს შემოვარტყათ გარშემო:

```html
<a>დააჭირე აქ</a>
```

შეიქმნა ლინკი, მაგრამ ალბათ შეამჩნევდით, რომ ამაზე დაჭერით რეაგირება არ აქვს. ამ ელემენტმა თავისით არ იცის რაზე გადავიდეს დაჭერით, ამიტომ მას უნდა მივუთითოთ სად უნდა გადავიდეს, ეს კი HTML ატრიბუტის დახმარებით კეთდება.

HTML ატრიბუტი აწვდის დამატებით ინფორმაციას ელემენტს და ატრიბუტი ყოველთვის ჯდება ელემენტის გამხსნელ თეგში. ატრიბუტი ძირითადად შედგება ორი ნაწილისგან: სახელისგან და მნიშვნელობისგან(value). მაგრამ ყველა ატრიბუტს არ სჭირდება მნიშვნელობა. ჩვენს შემთხვევაში უნდა დავამატოთ `href` (hypertext reference) ატრიბუტი გამხსნელ `<a>` თეგს, ხოლო `href`-ის მნიშვნელობაში ვწერთ სად გვინდა ჩვენმა ლინკმა გადაგვიყვანოს.

დაანატე ეს href ატრიბუტი ანქორ ელემენტს, რომელიც უკვე გავაკეთეთ და სცადეთ ახლიდან დაჭერა, არ დაგავიწყდეთ დაარეფრეშოთ ბრაუზერი, რათა ცვლილებები კოდში ჩაიტვირთოს.

```html
<a href="https://www.xazy.ge/about">დააჭირე აქ</a>
```

ჩვეულებისამებრ, თუ ტექსტს ანქორ თეგს შემოვარტყავთ `href` ატრიბუტის გარეშე, უბრალოდ ტექსტი გამოჩნდება. თუ `href` ატრიბუტი არსებობს, ბრაუზერი მას მისცემს ლურჯ ფერს და ქვევით ექნება ხაზი, რომელიც ლინკის მიმანიშნებელია.

ასევე აღსანიშნავია, რომ თქვენ შეგიძლიათ გამოიყენოთ ლინკთან ნებისმიერი რესურსი ინტერნეტიდა, არა მხოლოდ HTML დოკუმენტები. შეგიძლიათ დალიკნოთ ვიდეოები, pdf ფაილები, ფოტოები და ა.შ. მაგრამ ძირითად შემთხვევაში თქვენ HTML დოკუმენტებს დაუკავშირებთ.

## ლინკის ახალ ტაბში გახსნა

ზედა მეთოდი, რომელიც ვისწავლეთ, ლინკს იმავე ტაბში ხსნის. ის ყოველთვის ამას იზავს და ამის შეცვლა, ისე, რომ ახალ ტაბში გაიხსნას ლინკი ძალიან მარტივად შეიძლება, მხოლოდ `target` ატრიბუტი გვჭირდება.

`href` აძლევს ლინკს მითითებას სად გადავიდეს, ხოლო `target` აზუსტებს როგორ გაიხსნას დალინკული რესურსი, თუ ეს უკანასკნელი არ გვაქვს, მისი მნიშვნელობა აყენია `_self`-ზე, რომელიც იმავე ტაბში ხსნის ლინკს. იმისათვის, რომ ეს ლინკი ახალ ტაბში გავხსნათ მისი მნიშვნელობა უნდა იყოს `_blank`:

```html
<a href="https://www.xazy.ge/about" target="_blank" rel="noopener noreferrer">დააჭირე აქ</a>
```

ალბათ შეამჩნევდით, როგორ შევაპარეთ `rel` ატრიბუტი. ეს ატრიბუტი იმისათვის გამოიყენება, რომ აღწეროს ურთიერთობა ახლანდელ გვერდსა და დალინკულ დოკუმენტს შორის.

`noopener` მნიშვნელობა უზრუნველყობს იმას, რომ გახსნილმა ლინკმა არ მიიღოს წვდომა იმ გვერდზე, რომლიდანაც გაიხსნა. `noreferrer` მნიშვნელობა უზრუნველყოფს, რომ გახსნილმა ლინკმა ვერ გაიგოს რომელ ვებგვერდზე ან რესურსზეა ეს ლინკი მიმაგრებული. მათი გამოყენება ცალ-ცალკეც შეიძლება.

რატომ გვჭირდება ეს დამატებითი ქცევების მითითება ლინკის ახალ ტაბში გასახსნელად? უსაფრთხოების გამო. `noopener` აღმოფხვრავს [ფიშინგს](https://ka.wikipedia.org/wiki/%E1%83%A4%E1%83%98%E1%83%A8%E1%83%98%E1%83%9C%E1%83%92%E1%83%98), როდესაც გახსნილი ლინკზე ჩაიტვირთოს ყალბი საიტი, მომხმარებლების შეცდომაში შესაყვანად. ეს ცნობილია როგორც [tabnabbing](https://owasp.org/www-community/attacks/Reverse_Tabnabbing). `noreferrer` მნიშვნელობა მაშინ შეგვიძლია გამოვიყენოთ, როცა გსურთ გახსნილ ლინკს არ გააგებინოთ რომელ ვებსაიტზე იყო ეს ლინკი განთავსებული.

ყველაფერი კარგად იქნება, თუ დაგავიწყდებათ `rel="noopener noreferrer"`, რადგან ბრაუზერის უახლესი ვერსიები ამ უსაფრთხოებას "აყოლებენ" თუ `target="_blank"` სახეზეა. მაგრამ მაინც სიფრთხილისთვის, რეკომენდირებულია, რომ `target="_blank"`-ს მიაწეროთ `rel="noopener noreferrer"`.

## Absolute და Relative ლინკები

ჩვენ ორი სახის ლინკებს შევქმნით:

- ლინკები, რომლებიც სხვა ინტერნეტის ვებგვერდებზე გადადის.
- ლინკები, რომლებიც ჩვენი ვებსაიტის გვერდებზე გადადის.

### Absolute ლინკები 

იმ გვერდების ლინკები, რომლებიც ინტერნეტის სხვა ვებგვერდებზე გადადის არის absolute ლინკები. ჩვეულებრივი ასეთი ლინკი შედგება შემდეგი ნაწილებისგან: `protocol://domain/path`. მას აუცილებლად უნდა ჰქონდეს პროტოკოლი და დომეინი იმ გვერდის, რომელზეც გადადის.

ჩვენ უკვე გვაქვს ერთი ასეთი ლინკი შექმნილი, რომელიც ხაზის "ჩვენს შესახებ" გვერდზე გადადის. ის შეიცავს პროტოკოლს და დომეინს.

`https://www.xazy.ge/about`

### Relative ლინკები

ლინკები სხვა გვერდებზე, რომლებიც ჩვენს ვებსაიტზეა, ჰქვიათ relative ლინკები. ისინი არ შეიცავენ დომეინის სახელს, რადგან ეს სხვა გვერდი ამავე საიტზეა და თავისით ხვდება, რომ დომეინის სახელი იგივე იქნება, რაც ამ საიტის დომეინია.

Relative ლინკები მხოლოდ ამ გვერდამდე მისასვლელ ფაილის სახელს შეიცავს.

`index.html`-სთან ერთად, იმავე ფოლდერში, შექმენით `about.html` ფაილი და ჩასვით ეს კოდი:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>ლინკები და ფოტოები</title>
  </head>

  <body>
    <h1>ჩვენს შესახებ</h1>
  </body>
</html>
```

ახლა დაბრუნდით ისევ `index` გვერდზე და შექმენით მოცემული ენქორ ელემენტი, სადაც ორივე სახის ლინკი იქნება გამოყენებული.

```html
<body>
  <h1>ჩვენს შესახებ</h1>
	<a href="https://www.xazy.ge/about">დააჭირე აქ</a>

	<a href="about.html">ჩვენს შესახებ</a>
</body>
```

გახსენით index ფაილი ბრაუზერში და დააჭირეთ ორივე ლინკს, რომ შეამოწმოთ, სწორად მუშაობს თუ არა. ლინკზე დაჭერისას უნდა გადადიოდეს ჩვენს შექმნილ about გვერდზე.

ეს იმიტომ მუშაობს, რომ index და about გვერდები ერთი და იმავე ფოლდერშია. ეს ნიშნავს რომ ჩვენ შეგვიძლია მისი სახელი (`about.html`) გამოვიყენოტ ლინკის href მნიშვნელობად.

მაგრამ ჩვეულებრივ, ჩვენ გვინდა რომ უკეთ დავაორგანიზოთ ვებსაიტის გვერდები.

იმავე ფოლდერში შექმენით კიდევ ახალი ფოლდერი, სახელად `pages` და მასში ჩააგდეთ `about.html`.

დაარეფრეშეთ index გვერდი ბრაუზერში და ახლიდან დააჭირეთ მოცემულ ლინკს. ნახავთ, რომ ეს ლინკი აღარ მუშაობს. ეს იმიტომ ხდება, რომ about გვერდის ფაილის ლოკაცია შეიცვალა.

ამის გასასწორებლად უნდა განვაახლოთ about ლინკის href-ის მნიშვნელობა და მივუთითოთ `pages/` ლოკაცია, რადგან ეს ფაილი მასშია.

```html
<body>
  <h1>ჩვენს შესახებ</h1>
	<a href="pages/about.html">About</a>
</body>
```

ახლა ისევ დაარეფრეშეთ ინდექს გვერდი და დააჭირეთ ლინკს ახლიდა, ახლა ყველაფერმა სწორად უნდა იმუშაოს.

ბევრ შემთხვევაში ეს უპრობლემოდ იმუშავებს, მაგრამ, თქვენ შეიძლება შეგხვდეთ პრობლემები ასეთი მიდგომით. წინ `./`-ის დაწერა ასეთ პრობლემებს აღმოფხვრავს. წინ `./`-ის დამატებით კოდს მივუთითებთ, რომ იმ ფაილის/ფოლდერის ძებნა დაიწყოს იმავე ფოლდერში, რომელშიც index ფაილი გვაქვს.

```html
<body>
  <h1>ჩვენს შესახებ</h1>
  <a href="./pages/about.html">ჩვენს შესახებ</a>
</body>
```

### მეტაფორა

Absolute და relative ლინკები, ცოტათი გაუგებარია დამწყებთათვის, ამიტომ უკეთ გასაგებად შესაძლოა ეს მეტაფორა დაგეხმაროთ:

წარმოიდგინეთ დომეინის სახელი (`ქალაქი.ge`) ქალაქად. ფოლდერი, რომელშიც შენი ვებსაიტია (`/მუზეუმი`) მუზეუმად და თითოეული გვერდი, თქვენს ვებსაიტზე მუზეუმის ოთახებად (`/მუზეუმი/კინოს_ოთახი.html` და `/მუზეუმი/მაღაზიები/ყავის_მაღაზია.html`). Relative ლინკები, მაგალითად, `./მაღაზიები/ყავის_მაღაზია.html` არის მიმართულება იმავე ოთახიდან (მუზეუმის კინოს ოთახი `/მუზეუმი/კინოს_ოთახი.html`) სხვა ოთახამდე (მუზეუმის მაღაზია). Absolute ლინკები, სხვაგვარად, არის სრული მიმართულება პროტოკოლის (`https`), დომეინის სახელის (`ქალაქი.ge`) და ამ დომეინიდან მიმართულების ჩათვლით (`/მუზეუმი/მაღაზიები/ყავის_მაღაზია.html`): `https://ქალაქი.ge/მუზეუმი/მაღაზიები/ყავის_მაღაზია.html`.

## სურათები

ვებგვერდები ძალიან მოსაწყენი იქნებოდა მხოლოდ ტექსტის ჩვენება რომ შეეძლოთ. საბედნიეროდ HTML გვაწვდის სხვადასხვა მედია საშუალებების საიტზე გამოჩენის შესაძლებლობას. მათგან ყველაზე გავრცელებული კი სურათის ჩასასმელი ელემენტი.

იმისათვის, რომ სურათი თქვენს HTML გვერდზე გამოაჩინოთ, საჭიროა `<img>` ელემენტი. სხვა ელემენტებისგან განსვავებით, რომლებიც აქამდე გამოგვიყენებია, `<img>` ელემენტი არის თვით-დახურვადი, ანუ არ სჭირდება დამხურავი თეგი.

კონტენტის გამხსნელ და დამხურავ თეგში შემორტყმის ნაცვლად, თავად ამ ტაგს გადაეცემა ფოტოს მისამართი `src` ატრიბუტის გამოყენებით, რომელიც ეუბნება ბრაუზერს სურათის მდებარეობას. `src` ატრიბუტი მუშაობს როგორც `href` ატრიბუტი `<a>` თეგისთვის. მას შეუძლია მიიერთოს როგორც absolute, ასევე relative გზით.

მაგალითისთვის, absolute გზით გვერდზე შეგვიძლია გამოვიყენოთ ხაზის საიტზე არსებული ფოტო:

<iframe height="300" style="width: 100%;" scrolling="no" title="absolute-path-image" src="https://codepen.io/xazy/embed/ExMKYJm?default-tab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/xazy/pen/ExMKYJm">
  absolute-path-image</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

1. სამუშაო ფოლდერში შევქმნათ ახალი ფოლდერი სახელად `images`.
2. ჩავიწეროთ [ეს ფოტო](https://images.unsplash.com/photo-1517849845537-4d257902454a?ixlib=rb-4.0.3&q=85&fm=jpg&crop=entropy&cs=srgb&dl=charlesdeluvio-Mv9hjnEUHR4-unsplash.jpg&w=640) და ჩააგდეთ ჩვენს შექმნილ `images` ფოლდერში.
3. შეცვალეთ ამ ფოტოს სახელი და დაარქვით `dog.jpg`.

ახლა კი დაამატეთ ფოტო `index.html` ფაილში:

```html
<body>
  <h1>ჩვენს შესახებ</h1>
	<a href="https://www.xazy.ge/about">დააჭირე აქ</a>

	<a href="./pages/about.html">ჩვენს შესახებ</a>

    <img src="./images/dog.jpg">
</body>
```

ახლა შეინახეთ `index.html` და გახსენით ბრაუზერში შედეგის სანახავად.

## მშობელი ფოლდერები

რა უნდა ვქნათ იმ შემთხვევაში, თუ ჩვენ გვსურს ძაღლის ფოტოს გამოყენება `about.html` ფაილში? ამისთვის უნდა გამოვიდეთ ერთი ფოლდერით უკან, რომ მოვხვდეთ მშობელ ფოლდერში.

იმისათვის, რომ უკანა, მშობელ ფოლდერში გავიდეთ, უნდა გამოვიყენოთ ორი წერტილი მიმართულებაში: `../`. ახლა ვნახოთ ეს მოქმედებაში. გავხსნათ `about.html` ფაილი და `<body>` თეგში დავამატოთ შემდეგი:

```html
<img src="../images/dog.jpg">
```

ჩავშალოთ დეტალურად:

1. პირველ რიგში მივდივართ ამ ფოლდერის მშობელ ფოლდერში, ანუ `image-and-link`-ში.
2. შემდეგ, როდესაც მშობელ ფოლდერში გადავედით, შეგვიძლია შევიდეთ `images` ფოლდერში.
3. საბოლოოდ, ჩვენ გვაქვს წვდომა `dog.jpg` ფაილზე.

ზევით აღნიშნულ მეტაფორას რომ შევადაროთ, `../` ნიშნავს გამოხვიდე იმ ოთახიდან, რომელ ოთახშიც ხარ და გახვიდე დერეფანში, საიდანაც სხვა ოთახში შეხვალ.

## Alt ატრიბუტი

`src` ატრიბუტთან ერთად, ყველა `img` ელემენტს ასევე უნდა ჰქონდეს `alt` (alternative text - ალტერნატიული ტექსტი) ატრიბუტი.

`alt` ატრიბუტი გამოიყენება იმისათვის, რომ აღწეროს სურათი. ეს ტექსტი მხოლოდ იმ შემთხვევაში იქნება გამოყენებული, თუ სურათი არ ჩაიტვირთება.

ასე გამოიყურება ხაზის ლოგოს მაგალითი, ოღონდ `alt`-ის დამატებით:

<iframe height="300" style="width: 100%;" scrolling="no" title="image-alt-attribute" src="https://codepen.io/xazy/embed/YzgqzXJ?default-tab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/xazy/pen/YzgqzXJ">
  image-alt-attribute</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

გავარჯიშებისთვის, დაამატეთ `alt` ატრიბუტი ძაღლის ფოტოს, რომელიც უკვე გამოვიყენეთ.

## სურათის ზომის ატრიბუტები

ეს არ არის აუცილებელი, მაგრამ სიმაღლისა(height) და სიგრძის(width) ატრიბუტების გამოყენება ეხმარება თეგს მისცეს ზომები.

ეს არ არის ხშირად გამოყენებული პრაქტიკა და ამ ზომების შესწორებას მოგვიანებით CSS-ს გამოყენებით ვისწავლით.

ეს არის ხაზის ლოგოს მაგალითი სიმაღლისა და სიგანის გამოყენებით:

<iframe height="300" style="width: 100%;" scrolling="no" title="image-height-and-with-attributes" src="https://codepen.io/xazy/embed/gOErOPy?default-tab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/xazy/pen/gOErOPy">
  image-height-and-with-attributes</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>


ახლა მიუთითეთ თქენს მიერ ჩასმულ ძაღლის ფოტოს სიმაღლე და სიგანე.

## დავალება

<div className="homework">

1. შექმენით ახალი ფოლდერი, რომელშიც იქნება `index.html`.
2. ამავე ფოლდერში შექმენით `about` და `gallery` ფოლდერები, თითოეულში ფოლდერის სახელის შესაბამისი ფაილი `.html` დაბოლოებით.
3. ასევე ფოლდერში შექმენით `images` ფოლდერი და მოათავსეთ რამდენიმე ფოტო.
4. `index.html` ფაილში შექმენით ლინკები, რომლებიც `about.html` და `gallery.html`-ზე გადავა ლინკით, ერთი იმავე ტაბში გაიხსნას, მეორე ახალ ტაბში.
5. `about.html` ფაილში ჩასვით ლინკები, რომლებზეც სხვა ვებსაიტებზე გადავა.
6. `gallery.html`-ში ჩასვით `images` ფოლდერში არსებული ფოტოები.

</div>

## დამატებითი რესურსები

ეს სექცია არაა აუცილებელი, მაგრამ ჩათვალეთ კლასგარეშე საკითხავად.

- [Links and images of HTML & CSS Is Hard](https://internetingishard.netlify.app/html-and-css/links-and-images/)
- [Chris Coyier's When to use target="_blank" on CSS-Tricks](https://css-tricks.com/use-target_blank/)
