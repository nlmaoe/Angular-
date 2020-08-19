# Angular гарын авлага

## Агуулга

- [Angular гэж юу вэ?](#Angular-гэж-юу-вэ)
- [Angular CLI хэрхэн суулгах вэ?](#Angular-CLI-суулгах-нь)
- [Angular CLI дээр хэрхэн project үүсгэх вэ?](#Angular-CLI-дээр-project-үүсгэх-нь)
- [Angular архитектур болон бүтэц](#Angular-архитектур-болон-бүтэц)

---

## Angular гэж юу вэ?

- Angular бол JavaScript фреймворк бөгөөд вэб аппликейшн бүтээхэд зориулагдсан.

- **Angular CLI** нь project шинээр үүсгэх, тест хийх, файл нэмэх, хөгжүүлэгч орчинд deployment хийх гэх мэт боломжуудыг агуулж эдгээрийг terminal/console орчноос коммандаар ажиллуулагч багаж юм.

- Гарал, үүсэл түүхийн талаар товчхон судлан үзвэл анх **Miško** Hevery болон **Adam Abrons** нар 2009 онд AngularJS буюу Angular 1 хувилбар төслийг хөгжүүлсэн. **Abrons**-ын хувьд энэхүү төслийг орхин гарсан бол **Hevery** нь Google компанид орон ажлын багийн нөхөдтэй цуг үргэлжлүүлэн хөгжүүлсэн. 

[Дээшээ буцах](#Angular-гарын-авлага)

---

## Angular CLI суулгах нь:

- Хэрэв таны компьютерт **Node.js** суулгаагүй бол [эндээс](https://nodejs.org/en/) суулгана уу. 

* Node.js суусан эсэхийг шалгахыг хүсвэл Command prompt-ыг онгойлгон **node -v** гэж бичин шалгах боломжтой.

<img src="pic/node.png" alt="node" width="50%" height="160" style="margin-left:10%"/>

- Үүний дараа Command  prompt дээрээ **npm install -g @angular/cli** гэж бичин enter товчийг дарж Angular CLI суулгах процессыг эхлүүлнэ. 

<img src="pic/npm.png" alt="npm" width="50%" height="230" style="margin-left:5%"/>

>Дээрх коммандууд бүрэн ажиллаж дуусахад багагүй хугацаа шаардах тул тэвчээртэй хүлээх хэрэгтэй.

- _Angular CLI_ суусан эсэхийг шалгахыг хүсвэл Command prompt дээр **ng v** гэж бичин шалгах боломжтой.

<img src="pic/cli.png" alt="Kitten" width="50%" height="300" style="margin-left:10%"/>

 - Үүнээс гадна хөгжүүлэгчид бидэнд ямар project/кодчилол хөгжүүлэгч программ ашиглаж цаг хэмнэх болон илүү өргөн боломжуудыг ашиглах зэрэг нь чухал зүйлүүд билээ. Angular project хөгжүүлэхэд тохиромжтой программ бол **Visual Studio code** юм.

* Учир нь бүх үйлдлийн систем дээр ажилладаг ба debug хийх, олон тооны terminal/console ашиглах, алдартай plugin/extension-үүдийг ашиглахад хялбар гэх мэт өргөн боломжуудыг агуулсан байдаг. [Link](https://visualstudio.microsoft.com/downloads/)

[Дээшээ буцах](#Angular-гарын-авлага)

---

## Angular CLI дээр project үүсгэх нь:

- Эхлээд шинээр folder үүсгэнэ. Дараа нь vscode-ыг уншуулан тэрхүү folder-ыг онгойлгоно.

<img src="pic/folder.png" alt="folder" width="65%" height="350" style="margin-left:5%"/>

- Үүний дараа vscode-ын terminal-ыг ажиллуулна.

<img src="pic/ter.png" alt="ter" width="65%" height="320" style="margin-left:5%"/>

- Тerminal дээрээ **ng new** _project name_ гэж бичин project үүсгэнэ.
 
- Дараа нь **cd** _project name_ гэж бичин тухайн project-ийн директор дотор орно.

- Project-доо ажиллуулахын тулд **ng serve** гэж terminal дээр бичин ажиллуулна.

- **ng serve** комманд нь сервер программыг ажиллуулж мөн тухайн project доторх файлуудыг ажиглаж байдаг ба шинэ өөрчлөлт орсон үед автоматаар дахин project-г build хийдэг. 

- Үүний дараа өөрийн ашиглаж буй вэб хөтөч дээрээсээ **localhost:4200**-луу хандана. 

- Хэрэв таньд тухайн **project app works!** мессежээр мэндчилж байвал таньд баяр хүргэе! та анхны алхмыг амжилттай гүйцэтгэлээ :)

[Дээшээ буцах](#Angular-гарын-авлага)

---

## Angular архитектур болон бүтэц

- HTML template-үүдийг Angular-жсан тэмдэглэгээт хэлээр **(ngFor, {{name}} , (click) etc.. )** бичиж , үүнийгээ **component** классуудаар өгөгдлийн эргэх холбоо буюу **data  binding** хийх зарчмаар удирдуулна. 

- Ингэхдээ **metadata** дотор ямар нөхцөл байдалд юуг агуулж болох талаар тодорхойлж бичсэнээр Angular хэрхэн тухайн component классыг ажиллуулах тухайгаа мэдэж авдаг. 

<img src="pic/com.png" alt="Kitten" width="50%" height="300" style="margin-left:5%"/>

- **Application logic** буюу программ хэрхэн ажиллах талаарх бүр нарийн логик дэс дарааг **service класс** дотор тусгаж тооцооллыг хийнэ. 

- Хэдийгээр **application logic**-г component класс дотор оруулах боломжтой ч бид олон удаа ашиглагдах шаардлагатай өгөгдөл эсвэл функцуудыг дахин дахин тодорхойлон үүсгэхээс зайлс хийх зорилготойгоор **service классыг** ашиглах ёстой. 

- Үүний тулд **dependency injection** гэх ойлголтыг хэрэглэдэг. Эдгээр **component** болон **service классуудыг** нэгтгэн хайрцаглаж **module** дотор оруулна. 

- Дараагийн алхам бол нийт **module**-ууд дундаас эхлэл болсон **root module** -г сонгон үүнийгээ **bootstrapping** хийн программаа ажиллуулна.

>Жишээ:

- Module

```
root -> src/app/app.module.ts
bootstrapping -> src/main.ts
```

- Service

```
src/app/employee.service.ts
```

- Components

```
src/app/app.component.ts
src/app/department.component.ts
src/app/employees.component.ts
```

- HTML templates

```
src/app/app.component.html
src/app/department.component.html
src/app/employees.component.html
```

[Дээшээ буцах](#Angular-гарын-авлага)

---

## Зөвлөмж

- Алхам алхмаар ахих түвшний хичээлүүдийг бүрэн судлаж мэдлэгээ зузаатгана уу.
- Angular сурах хэцүү санагадаж байвал Html , Css , Javascript-ын мэдлэгээ зузаатгаарай.
