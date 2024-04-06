# ტრანზიციები

## შესავალი

დადგა დრო, ვისწავლოთ CSS ტრანზიციები, რომლებიც ჩვენს HTML ელემენტებს ლამაზ ტრანსფორმაციებს დაადებს.

## გაკვეთილის მიმოხილვა

- რა არის CSS ტრანზიცია და როდის გამოვიყენოთ ის.
- რომელ სტილები შეიძლება იყოს ანიმაციური და რომელი არა.
- როგორ დავრწმუნდეთ ჩვენი ტრანზიციების კარგად მუშაობაში.

## ტრანზიციები

CSS ტრანზიციები საშუალებას გვაძლევს შევცვალოთ ელემენტის გარეგნობა. წარმოიდგინეთ ჩვეულებრივი ღილაკი თეთრი ფონით. როდესაც კურსორი არ გაქვთ ღილაკთან, ჩვეულებრივადაა და მოსაწყენია. როდესაც კურსორს ღილაკთან მივიტანთ, ღილაკის ფერი ნელ-ნელა გადავა ჯერ ნაცრისფერში, შემდეგ შავში, რაღაც დროის განმავლობაში. ეს არის CSS ტრანზიცია. ნახეთ ეს მაგალითი:

<iframe height="300" style="width: 100%;" scrolling="no" title="CSS Transition (longhand)" src="https://codepen.io/xazy/embed/gOyobvo?default-tab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/xazy/pen/gOyobvo">
  CSS Transition (longhand)</a> by XazyProject (<a href="https://codepen.io/xazy">@xazy</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

როდესაც მაუსის კურსორი არ არის ღილაკთან, ღილაკი ჩვეულებრივ მდგომარეობაშია. როდესაც მივიტანთ, სხვა მდგომარეობაში გადადის, hover მდგომარეობაში, რაც ფერის სასიამოვნო ტრანზიციას იწვევს. ფერი, გადასვლის დრო და ა.შ. ჩვენით შეგვიძლია ავირჩიოთ.

ეს `transition` სტილის დახმარებით გაკეთდა, რომელიც არის შემოკლებული ვარიანტი და გაერთიანებულია `transition-property`, `transition-duration`, `transition-timing-function` და `transition-delay` ფუნქციები.