
![](./images/banner.jpg)

# a. Các bài học 

## Bố cục các tệp trong dự án LaTeX: 


---

## Cấu trúc soạn thảo của LaTeX:

. . . 

---

## Viết từ "TeX" và "LaTeX" trong LaTeX:

Trong một số tài liệu ghi chép về LaTeX, người dùng có thể thấy tác giả viết từ "TeX" và "LaTeX" rất khác so với các từ khác như trong hình ảnh minh họa sau đây. 
. . . (hình minh họa)

Để làm được điều này, người dùng chỉ cần thêm kí tự `\` (kí tự này rất quan trọng về các bài học như [kí tự đặc biệt]()) vào trước từ TeX và cũng như là LaTeX. Cụ thể ta có lệnh đầy đủ sau đây

```latex
\TeX{} 
\LaTeX{}
```

hoặc cũng có thể là 

```latex
\TeX\ 
\LaTeX\
```

Điểm khác biệt ở hai câu lệnh trên tuy là ở sau từ TeX và LaTeX có thêm dấu ngoặc ngọn `{}` hoặc dấu `\`, nhưng kết quả cho ra được vẫn sẽ là giống nhau. 

$$\LaTeX{}, \ \TeX{}$$

Mục đích của dấu ngoặc nhọn hoặc kí tự `\` cần được thêm vào sau lệnh `\TeX`, `\LaTeX` là nhằm để hệ thống sẽ không tự động lấy mất khoảng trắng (dấu cách) khi người dùng viết tiếp câu văn ngay sau từ LaTeX đó.

Để dễ hình dung, người dùng xem qua ví dụ đoạn mã sau đây về việc nếu như người dùng không thêm dấu ngoặc hay dấu `\` vào sau  lệnh \LaTeX`

```latex
\documentclass{article} 
\usepackage[utf8]{vietnam}
\begin{document} 
\LaTeX là một trình soạn thảo văn bản tuyệt vời. 
\end{document}
```

Người dùng có thể thấy dù chúng ta có nhấn dấu cách (nút space) trên bàn phím bao nhiêu lần, thì từ "là" vẫn sẽ bị dính liền với từ trước của nó là từ "LaTeX" . 
 
---

## Căn lề trang tài liệu:

Chúng ta có thể thay đổi khoảng cách căn lề (margin size) bằng cách sử dụng package `geometry` hỗ trợ. Package này sẽ tự làm mọi thứ bằng lệnh:

```latex
\usepackage[option]{geometry} 
```

trong đó:

- option: là các tham số được truyền vào để thiết lập kích thước trang giấy tài liệu mà người dùng mong muốn.

Các option phổ biến thường thấy bao gồm:

- Chọn kích thước trang giấy (page size): a4papper, a5paper, letterpaper, ..vv..
- Định lề trang (margins): margin =... (đặt tất cả các lề), top = . . . (lề trên), left = . . .(lề trái), right = . . .(lề phải), bottom = . . . (lề dưới).
- Hướng giấy (Orientation): portrait (khổ dọc), landscape (khổ ngang).

Ví dụ: Đặt tất cả các lề của trang đều bằng 1in

```latex
\usepackage[margin=1in]{geometry}
```

---
## Chú thích trong LaTeX:

Để chú thích trong LaTeX ta sử dụng kí hiệu `%`:

```latex
% chú thích 
```

--- 
## Kí tự thông thường: 

Các kí tự thông thường là các kí tự mà người dùng có thể nhập trực tiếp từ bàn phím có thể xuất sang trang tài liệu mà không cần sử dụng thêm câu lệnh gì. 

Các kí tự thông thường trong LaTeX bao gồm:
- In hoa A - Z
- In thường a - z
- Số 0 - 9
- Các kí tự ngắt nghỉ câu (?)
--- 
## Kí tự đặc biệt:

Thuật ngữ "kí tự đặc biệt" dùng để chỉ tất cả các kí hiệu ngoại trừ các chữ cái viết thường, in hoa, các chữ số và các kí tự ngắt nghỉ câu mà ta đã nhắc ở [kí tự thông thường](). 

Hơn nữa, các kí tự đặc biệt cũng là các kí tự mà người dùng đôi khi không thể nhập trực tiếp được từ bàn phím vào phần soạn thảo LaTeX. Vì một số kí hiệu đó đã được dành riêng để có chức năng phục vụ cho mục đích nào đó của LaTeX. 

Ví dụ như kí tự $\text{\%}$ dùng để [chú thích trong LaTeX](). Nếu như người dùng gõ trực tiếp dấu chú thích đó vào phần soạn thảo LaTeX, thì khi xuất ra trang tài liệu, chúng sẽ không được hiện hữu trong trang tài liệu, mà thay vào đó hệ thống chỉ hiểu kí tự $\text{\%}$ đó đang được dùng để chú thích trong phần soạn thảo.  

```latex
\documentclass{article}

% --- Cấu hình ngôn ngữ tài liệu ---
\usepackage[english]{babel}

\begin{document}

% --- Khai báo thông tin bài viết ---
\title{Your Paper}
\author{You}
\date{\today}

% --- Hiển thị tiêu đề, tác giả, ngày tháng ---
\maketitle

% Nếu viết trực tiếp kí tự % , LaTeX sẽ hiểu đó là chú thích mà không xuất hiện ở trong trang tài liệu 

\end{document}
```

Điều này cũng tương tự đối với các kí tự sau $\textbackslash$, ...vv...

Hoặc đôi khi người dùng sẽ thấy nó còn báo lỗi nếu như người dùng gõ các kí tự đặc biệt đó một cách trực tiếp trong phần biên soạn như ví dụ về kí tự viết [toán học nội tuyến]() sau. 

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tài liệu ---
\usepackage[english]{babel}

\begin{document}
% --- Khai báo thông tin bài viết ---
\title{Your Paper}
\author{You}
\date{\today}
% --- Hiển thị tiêu đề, tác giả, ngày tháng ---
\maketitle
% Nếu viết hai lần kí tự $ $, LaTeX sẽ hiểu là người dùng đang viết toán học nội tuyến (inline math)
$ $
% Nếu viết đơn lẻ kí tự &, LaTeX sẽ báo lỗi "Misplaced alignment tab character &".
& 
\end{document}
```

Nếu người dùng chạy đoạn mã trên trực tiếp trên Texlive.net hoặc Overleaf, chúng đều báo cùng một lỗi là "Misplaced alignment tab character &". 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img5.1.jpg"
         alt="Báo lỗi ở Texlive.net">
	<figcaption>Báo lỗi kí tự '&' ở Texlive.net</figcaption>
</figure>

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img5.2.jpg"
         alt="Báo lỗi ở Overleaf">
	<figcaption>Báo lỗi kí tự '&' ở Overleaf</figcaption>
</figure>

Tùy thuộc vào kí tự đặc biệt người dùng sử dụng đó mà hệ thống sẽ báo lỗi để người dùng biết nhằm khắc phục lỗi của kí tự đó. 

Để viết các kí tự đặc biệt đó xuất hiện ở trang tài liệu, người dùng cần phải thêm trước kí tự đặc biệt đó với kí tự `\`. 

Ví dụ:

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tài liệu ---
\usepackage[english]{babel}

\begin{document}
% --- Khai báo thông tin bài viết ---
\title{Your Paper}
\author{You}
\date{\today}
% --- Hiển thị tiêu đề, tác giả, ngày tháng ---
\maketitle
% Viết kí tự đặc biệt nhờ vào dấu '\' 
\% 
\_ 
\& 
\{ 
\} 
\end{document}
```

Đối với kí tự $\textasciicircum{}$, người dùng cần phải sử dụng lệnh sau

```latex
\textasciicircum 
```

Đối với kí tự $\textbackslash$,  người dùng cần phải sử dụng lệnh sau 

```latex 
\textbackslash
```

Một số kí tự đặc biệt mà người viết khuyên người dùng có thể chỉ cần gõ một cách trực tiếp các kí tự đó thì nó vẫn sẽ xuất hiện ở trang tài liệu mà không cần phải nhớ lệnh của chúng. 

Ví dụ: 

```latex

```

Các kí tự đặc biệt ở trên được tổng hợp đầy đủ ở bảng dưới đây mà người dùng có thể tham khảo:  



(xem ở đây https://en.wikibooks.org/wiki/LaTeX/Special_Characters#Other_symbols) 

---
## Các chữ cái đặc biệt: 

Các chữ cái đặc biệt là gì ? (tìm hiểu đôi chút về lịch sử các nước sử dụng nó cũng vui hihi)

Xem tại đây: https://en.wikibooks.org/wiki/LaTeX/Special_Characters 

--- 
## Định dạng thông tin cơ bản: 

Một số thông tin cơ bản mà người dùng cần thêm vào tài liệu khi viết bài báo, ...vv..  bao gồm:
- Tiêu đề tài liệu/bài viết
- Tác giả
- Ngày/tháng/năm (hoặc cũng có thể chỉ cần tháng/năm) xuất bản 

```latex
\title{Your title}
\author{You}
\date{Day/Mouth/Year}
```

Bên trong lệnh `\date{}`, người dùng có thể điền ngày/tháng/năm ở bất kì mốc thời gian cố định nào tùy ý. 

Các thông tin khai báo cơ bản ở trên gồm tiêu đề, tác giả, ngày/tháng/năm sẽ không được xuất hiện trong trang tài liệu cho tới khi người dùng sử dụng lệnh 

```latex
\maketitle
```

được đặt ở bên trong môi trường `documents`. 

Nếu như người dùng không sử dụng lệnh `\date` hoặc 

```latex
\date{\today}
```

thì ngày/tháng/năm sẽ được LaTeX tự động cập nhật theo thời gian thực mỗi khi người biên dịch (compile) tài liệu. 

Nếu như người dùng không muốn hiển thị thông tin ngày/tháng/năm ở trong tài liệu của mình, người dùng chỉ cần bỏ trống phần thông tin bên trong lệnh `\date`. 

```latex
\date{}
```

Để hiện thị thêm thông tin (như email, nơi công tác) của tác giả, người dùng chỉ cần thêm lệnh `\thanks{}` vào ngay bên trong lệnh `\author{}`. 

```latex
\author{You\thanks{Your information}}
```

Bên trong dấu ngoặc của lệnh `\thanks` là nơi người dùng cần thêm thông tin của tác giả đó. Lúc này, tên tác giả sẽ xuất hiện dưới dạng một dấu sao nằm ở trên đầu góc trái của tên tác giả đó và nội dung thông tin được cung cấp thêm cho tác giả sẽ được hiển thị ở chân trang tài liệu đó. 

Dưới đây là ví dụ hoàn chỉnh kết hợp các yếu tố trên. 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % latex Khai báo tài liệu viết Tiếng Việt

% Khai báo thông tin tài liệu
\title{An Example of LaTeX Document} 
\author{Namlete\thanks{nguyenlenam15082007@gmail.com}} 
\date{May 30, 2026} 

\begin{document}

% Lệnh bắt buộc để hiển thị tiêu đề, tác giả, ngày tháng ra màn hình
\maketitle

Hello LaTeX! Đây là nội dung bài viết của bạn.

\end{document}
```

Nếu như người dùng muốn thông tin tác giả được hiện thị ở ngay sau phần tên tác giả, đầu tiên người dùng cần khai báo package sau

```latex
\usepackage{authblk}
```

Sau đó, người dùng sử dụng hai lệnh sau: 

```latex
\author[]{}
\affil[]{}
```

trong đó: 
+ Lệnh `\author[]{}` là nơi người dùng cần điền tên tác giả
+ Lệnh `\affil[]{}` là nơi người dùng cần điền thông tin của tác giả đó. 

Dấu ngoặc vuông `[]` là nơi người dùng điền `option` là số thứ tự như $1, 2, 3, \dots$  hoặc các kí hiệu toán học, chữ cái Hy Lạp khác như $\dagger, \beta , \dots$ , để liên kết tác giả với thông tin của tác giả tương ứng, 

Ta có ví dụ về điều này như sau: 

```latex
\documentclass{article}

% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[english]{babel}
\usepackage{authblk}

\title{Your Paper}
\author[1]{You}
\affil[1]{Your information}
\date{}

\begin{document}
\maketitle
\end{document}
```
![](2026/IT-project/LaTeX-Library-project/1.0.0/Images/img3.1.jpg)

Người dùng cũng có thể sử dụng điều này để trình bày nhiều hơn một tác giả cộng tác tài liệu qua ví dụ sau:

```latex
\author[1]{author 1}
\author[2]{author 2}
\affil[1]{Author information 1}
\affil[2]{Author information 1}
```

![](LaTeX-Library-project-v1.0.0/images/img3.2.jpg)

--- 
## Đơn vị độ dài trong LaTeX:



---

## Lorem ipsum:

**Lorem ipsum** là một [đoạn văn bản giả hoặc văn bản giữ chỗ](https://en.wikipedia.org/wiki/Placeholder_text "Văn bản giữ chỗ")  thường được sử dụng trong thiết kế đồ họa, xuất bản và phát triển web. 

Nó thường là một phiên bản bị thay đổi của _[De finibus bonorum et malorum](https://en.wikipedia.org/wiki/De_finibus_bonorum_et_malorum "De finibus bonorum et malorum")_, một văn bản thế kỷ thứ nhất Trước Công nguyên của chính khách và triết gia La Mã [Cicero](https://en.wikipedia.org/wiki/Cicero "Cicero") , với các từ bị thay đổi, thêm vào và loại bỏ để làm cho nó trở nên vô nghĩa và không đúng ngữ pháp tiếng Latinh. Hai từ đầu tiên là [dạng rút gọn](https://en.wikipedia.org/wiki/Clipping_\(morphology\) "Cắt tỉa (hình thái học)") của _dolorem ipsum_ ("chính là nỗi đau"). Mục đích của lorem ipsum là cho phép thiết kế bố cục trang, độc lập với nội dung văn bản sẽ được điền vào sau đó, hoặc để minh họa các phông chữ khác nhau của một kiểu chữ mà không có văn bản có ý nghĩa gây mất tập trung.[^17] (Dịch tạm là vậy)

![[LaTeX-Library-project-v1.0.0/images/lorem Ipsum.jpg]]
(Nguồn ảnh: https://priceonomics.com/the-history-of-lorem-ipsum/)

Để sử dụng được đoạn văn bản giả Lorem ipsum ở trong LaTeX, trước tiên người dùng cần phải khai báo Package

```latex
\usepackage{lipsum} 
```

được đặt ở . . . (vị trí nào trong phần soạn thảo ?):

Sau đó người dùng chỉ cần đặt các lệnh sau vào phần . . . ( phần nào của soạn thảo ?)

Với lệnh 

```latex
\lipsum
```

hệ thống sẽ tự động xuất sang trang tài liệu khoảng bảy đoạn văn bản lorem ipsum mặc định.

```latex
\documentclass{article}
% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[english]{babel}
\usepackage{lipsum} 
\title{Your Paper}
\author{You}
\date{}
\begin{document}
\maketitle
\lipsum
\end{document}
```

Với lệnh 

```latex
\lipsum[1-150]
```

hệ thống sẽ tự động xuất sang trang tài liệu đầy đủ từ 1 đến 150  đoạn văn bản lorem ipsum mặc định. 

Nếu như người dùng để lệnh

. . . (có khoảng 150 văn bản lorem khác nhau, đây là giới hạn . . ., nếu như người dùng sử dụng

```latex
\lipsum[1000]
```

thì hệ thống sẽ tự động xuất sang trang tài liệu đoạn văn Lorem thứ 100. 

Lý do là bởi 

. . . 1000:150 . . . lấy ở đoạn văn Lorem thứ 100) 


---
## Thay đổi kích cỡ chữ: 

Để thay đổi kích cỡ chữ trong trang tài liệu, người dùng chỉ cần thêm thông số vào bên trong dấu ngoặc vuông `[]` ở phần khai báo lớp tài liệu (`documentclass`). 

Xem qua ví dụ đoạn mã dưới đây:

```latex
\documentclass[12pt]{article}
\usepackage{lipsum} % lorem ipsum
\begin{document}
\lipsum
\end{document}
```

người dùng có thể thấy bảy đoạn văn bản [lorem ipsum]() trong trang tài liệu đều sẽ có kích cỡ chữ là 12pt.  

Thông số được thêm vào bên trong dấu ngoặc vuông đó đối với LaTeX chỉ có thể được thay đổi đối với ba kích cỡ cơ bản là 10pt, 11pt và 12pt. 

Nếu như người dùng không thêm bất kì tùy chọn thông số nào làm thay đổi kích cỡ chữ, thì hệ thống sẽ mặc định để kích cỡ chữ trong trang tài liệu là 10pt. 

```latex
\documentclass{article}
\usepackage{lipsum} % lorem ipsum
\begin{document}
\lipsum
\end{document}
```

--- 

##  Tóm tắt bài báo: 

Trong LaTeX, các lớp tài liệu học thuật như **`article`** (bài báo) hay **`report`** (báo cáo), luôn có phần được gọi “tóm tắt”.

Để viết phần tóm tắt, người dùng cần sử dụng môi trường `abtract` với cú pháp sau. 

```latex
\begin{abstract}
    ... Nội dung tóm tắt của bạn viết tại đây ...
\end{abstract}
```

![](./images/img4.1.jpg)

Môi trường `abstract` này được đặt ngay sau lệnh `\maketitle`.

> [!WARNING]  
> Môi trường `abstract` này không thể được thực thi với các lớp tài liệu là `book`, `letter`, $\dots vv \dots$

Nếu như người dùng muốn thay đổi tiêu đề mặc định của LaTeX là "tóm tắt nội dung" (tiếng Việt) hay "abstract" (tiếng Anh), người dùng cần sử dụng lệnh sau: 

```latex
\renewcommand{\abstractname}{New Name}
```

Với lệnh này, tiêu đề ở phần tóm tắt sẽ được thay thế bằng bất kỳ từ nào khác mà người dùng cung cấp.  

Ví dụ minh họa về phần tóm tắt vào trong một tài liệu. 

```latex
\documentclass{article} 
\usepackage[utf8]{vietnam} % Khai báo tài liệu viết Tiếng Việt

% Khai báo thông tin tài liệu
\title{An Example of LaTeX Document} 
\author{Namlete} 
\date{May 30, 2026} 

\begin{document} 

% 1. Hiển thị tiêu đề, tác giả, ngày tháng bài viết 
\maketitle 

% 2. Hiển thị phần tóm tắt bài viết
\renewcommand{\abstractname}{Tóm tắt} % Thay đổi dòng "Tóm tắt nội dung" mặc định thành "Tóm tắt". 

\begin{abstract} 
    Đây là nơi bạn viết một đoạn tóm tắt ngắn gọn (khoảng 150-250 từ) 
    về mục tiêu, phương pháp và kết quả chính của bài nghiên cứu này.
\end{abstract} 

% 3. Nội dung chính của tài liệu
Hello LaTeX! 

\end{document}
```

---

## Viết tài liệu tiếng Việt 

Để viết tài liệu tiếng Việt, ta cần khai báo gói sau:

```latex
\usepackage[utf8]{vietnam}
```

Bộ encode **UTF-8** là package thông dụng để hiển thị các chữ cái Latin trong tiếng Anh, kể cả các chữ cái Hy Lạp và Việt Nam. (?)

---

## Ngắt trang

Để viết tài liệu sang một trang tài liệu mới, người dùng sử dụng lệnh sau: 

```latex
\newpage
```

---

## Xuống dòng văn bản: 

Người dùng chỉ cần nhấn phím **Enter** được nhập trên bàn phím hai lần, để làm văn bản được xuống dòng mới khi soạn thảo LaTeX. (? viết chưa rõ ý tưởng)

---

## Thụt lề đầu dòng các đoạn văn trong văn bản

Khi [xuống dòng văn bản]() trong LaTeX, hệ thống sẽ tự động thụt lề đầu dòng cho đoạn văn mới. 

Thông thường, hệ thống sẽ mặc định tự động thụt lề đầu dòng vào một khoảng 20pt. Tuy nhiên người dùng có thể tự căn chỉnh nó bằng cách thêm vào câu mở đầu lệnh có cú pháp như sau: 

```latex
\setlength{\parindent}{length}
```

trong đó:

- length: là kích thước thụt đầu dòng mà người dùng muốn khi đoạn văn xuống dòng.

Với length = 0, tất cả các đoạn văn đều trong trang tài liệu đều không được thụt lề đầu dòng. 

Kích thước thụt lề đầu dòng đoạn văn được . . . (bên đối tượng nào ?) khuyến nghị (nên thụt lề với khoảng cách là bao nhiêu khi viết tài liệu là hợp lí ?) . . . 

Nếu như người dùng muốn lựa chọn tùy ý việc để đoạn văn tiếp theo có hay không thụt đầu dòng, người dùng có thể sử dụng hai lệnh sau. Với 

```latex
\indent
```

được dùng để đoạn văn đó thụt đầu dòng. Và 

```latex
\noindent
```

được dùng để đoạn văn đó không thụt đầu dòng.

Cả hai lệnh `\indent` và `\noindent` đều phải được đặt ở trước đoạn văn mà người dùng mong muốn có hay không thụt đầu dòng. 

Kích thước thụt lề đầu dòng của lệnh `\indent` là 20pt (? viết lại chưa hiểu ý cho lắm )

---

## Khoảng cách giữa các đoạn văn trong văn bản:

Để tùy chỉnh khoảng cách giữa các đoạn, ta sử dụng lệnh
```latex
\setlength{\parskip}{#}
```

trong đó:

- \# là kích thước khoảng cách giữa các đoạn văn mà người dùng muốn khi đoạn văn xuống dòng.  

--- 

## Khoảng cách giữa các dòng trong đoạn văn:

Đầu tiên, người dùng cần phải khai báo package sau:

```latex
\usepackage{setspace}
```

Từ đây, người dùng có thể chọn một trong hai cách sau đây để thay đổi khoảng cách giữa các dòng.

**Cách 1**: Thêm những lệnh sau trước đoạn văn để thay đổi khoảng cách giữa các dòng

```latex
\singlespacing
\onehalfspacing 
\doublespacing
\setstretch{<float number>}
```

trong đó:

- `\singlespacing`: thay đổi khoảng cách giữa các dòng là bằng 1.
- `\onehalfspacing`: thay đổi khoảng cách giữa các dòng là bằng 1.5 .
- `\doublespacing`: thay đổi khoảng cách giữa các dòng là bằng 2.
- `\setstretch{<float number>}`: thay đổi được khoảng cách giữa các dòng tùy ý trong khoảng lớn hơn 1 và nhỏ hơn 2. 

**Cách 2**: Sử dụng môi trường spacing
```latex
\begin{spacing}
Văn bản
\end{spacing}
```

trong đó spacing có thể được thay thế bằng:

- `singlespace`: thay đổi khoảng cách giữa các dòng là bằng 1.
- `onehalfspace`: thay đổi khoảng cách giữa các dòng là bằng 1.5 .
- `doublespace`: thay đổi khoảng cách giữa các dòng là bằng 2.

Để thay đổi được khoảng cách giữa các dòng tùy ý trong khoảng lớn hơn 1 và nhỏ hơn 2, người dùng chỉ cần thêm bên cạnh `\begin{spacing}` là `{<float number>}`,  lúc này ta có:
```latex
\begin{spacing}{<float number>}
Khoảng cách gữa các dòng trong một đoạn văn được thay đổi bởi <float number>
\end{spacing}
```

Ví dụ sau đây . . .

---

## Căn lề cho đoạn văn bản:

Hệ thống LaTeX sẽ để căn lề mặc định cho đoạn văn bản là "[justified]()" (căn đều hai bên).  

Để có thể thay đổi căn lề cho đoạn văn bản, người dùng có thể sử dụng môi trường sau:
```latex
\begin{alignment type}
	Nội dung...
\end{alignment type}
```

Trong đó, alignment type có thể là:
<p align="left">
+ flushleft: Căn trái
</p>
<p align="right">
+ flushright: Căn phải
</p>
<p align="center">+ center: căn giữa</p>
Ngoài ra người dùng có thể đặt các lệnh sau: 

```latex
\raggedright % Căn trái
\raggedleft % Căn phải
\centering
```

vào trước các đoạn văn bản để được tùy chỉnh căn lề cho đoạn văn đó. 

. . . 

---

## In đậm, in nghiên, gạch chân chữ, chữ gạch giữa:

Đối với **in đậm**, người dùng sử dụng lệnh

```latex
\textbf{in đậm}
```

_In nghiêng_ thì sẽ là

```latex
\textit{in nghiêng}
```

Vậy vừa _**in đậm, in nghiêng**_ thì làm sao nhỉ ? Để làm được điều này, người dùng có thể lồng lệnh *in nghiêng* vào trong lệnh **in đậm** như sau 

```latex
\textbf{\textit{Vừa in đậm, vừa in nghiêng}}
```

Hoặc nếu như người dùng lồng lệnh `\textit` vào trong lệnh `\textbf`, thì kết quả cho ra được vẫn sẽ giống hệt với cách làm trên. 

Để <u>gạch chân chữ</u> (underline), người dùng sử dụng lệnh

```latex
\underline{Gạch chân chữ}
``` 

Đối với ~~chữ gạch giữa~~ (strikethrough), trước tiên người dùng cần phải khai báo package sau

```latex
\usepackage{soul}
```

sau đó để ~~chữ gạch giữa~~ người dùng sử dụng lệnh 

```latex
\st{Chữ gạch giữa}
```

. . . (Này là gì ? Có tác dụng gì ? Mục đích sử dụng ? Khi nào thì nên sử dụng ?)

```latex
\emph{}
```

Ví dụ với các đoạn văn sau 

```latex
Một số \emph{khám phá} vĩ đại nhất trong khoa học được thực hiện một cách tình cờ như . . .
```

Từ "khám phá" trong đoạn mã trên sẽ được *in nghiêng* so với các từ khác trong đoạn văn. 

```latex
\textit{Một số \emph{khám phá} vĩ đại nhất trong khoa học được thực hiện một cách tình cờ như . . .}
```

Từ "khám phá" trong đoạn mã trên sẽ không được in nghiêng so với các từ khác trong đoạn văn đang nằm trong lệnh `\textit{}` đang được *in nghiêng*. 

```latex
\textbf{Một số \emph{khám phá} vĩ đại nhất trong khoa học được thực hiện một cách tình cờ như . . .}
```

Từ "khám phá" trong đoạn mã vẫn sẽ được **in đậm** giống như các từ khác trong đoạn văn đang nằm trong lệnh `\textbf{}`, tuy vậy từ "khám phá" sẽ được *in nghiêng* so với các từ khác trong đoạn văn.  

--- 

## Màu chữ:[^8]

Đầu tiên người dùng cần phải khai báo package sau:

```latex
\usepackage{xcolor}
```

Package ở trên chỉ cho phép người dùng sử dụng được 19 màu cơ bản theo các tên màu đã được có sẵn mà không cần phải thêm bất kỳ `options` nào trong package như hình dưới đây.

![19 màu cơ bản](./images/img1.1.jpg)

Người dùng cũng có thể sử dụng thêm các màu ngoài 19 màu cơ bản trên theo ý muốn, cũng thông qua gói `xcolor` với các `options` như sau: 

1. `dvipsnames`: tải 68 màu được đặt tên (CMYK) 

```latex
\usepackage[dvipsnames]{xcolor}
```

![68  màu CMYK](./images/img1.2.jpg)

2. `x11names`: tải 317 màu được đặt tên (RGB) 
```latex
\usepackage[x11names]{xcolor}
```
![317 màu RGB ](./images/img1.3.jpg)

Để thay đổi màu sắc chữ người dùng sử dụng lệnh sau: 

```latex
\textcolor{color}{text}
```

trong đó:
- `color`: là nơi nhập tên màu sắc cho văn bản mà người dùng muốn, với điều kiện là màu được chọn phải phù hợp với `options` mà người dùng khai báo theo những hình ở trên.
- `text`: từ hoặc văn bản bị thay đổi thành màu mà người dùng lựa chọn. 

--- 

## Màu nền trang:

Người dùng cũng có thể thay đổi [màu]() nền của toàn bộ trang tài liệu tùy thích ngoài mặc định sẵn của LaTeX là trang tài liệu có màu trắng truyền thống, bằng cách sử dụng lệnh sau:

```latex
\pagecolor{color}
```

Lệnh này được đặt ở . . . 

---

## Nhập nền cho văn bản (highlight):

Để có thể tô đậm [màu]() cho đoạn văn bản, dòng văn bản hoặc các từ khóa quan trọng trong trang tài liệu, người dùng sử dụng lệnh sau:

```latex
\colorbox{color}{text}
```


---

## Tham chiếu chéo:  



---

## Lệnh phân cấp (Sectioning commands)

Đối với các lớp tài liệu (`documentclass`) như `article`, `proc`, `report`, `book`, `beamer`, chúng đều có các lệnh phân cấp nhằm tạo [mục lục]() để sắp xếp nội dung. 

Các lệnh phân cấp này không đứng ngang hàng với nhau, mà được sắp xếp theo một thứ tự ưu tiên từ cao xuống thấp

| Tên (Việt - Anh)              | Lệnh           | Cấp độ |
| :---------------------------- | -------------- | ------ |
| Phần (Part)                   | `\part{}`      | -1     |
| Chương (Chapter)              | `\chapter{}`   | 0      |
| Mục (Section)                 | `\section`     | 1      |
| Tiểu mục (Subsection)         | `\subsection{}`| 2      |
| Tiểu tiểu mục (Subsubsection) | `\subsubsection{}` | 3|
| Paragraph (Đoạn văn (có tiêu đề))| `\paragraph{}`  |  4 |
| Subparagraph (Đoạn văn (có tiêu đề) cấp nhỏ hơn)|`\subparagraph{}`| 5|

Tùy thuộc vào `documentclass` mà người dùng đang sử dụng mà thứ tự cấp độ ở bảng trên sẽ có chút thay đổi. 

Cụ thể, lệnh `\chapter` chỉ khả dụng trong các lớp tài liệu là `report` và `book`, mà không thể được sử dụng đối với lớp tài liệu là `article`, `proc`. 

Nếu như người dùng cố gắng viết lệnh `\chapter` vào phần soạn thảo LaTeX đang ở lớp tài liệu như `article`, `proc`, thì hệ thống sẽ báo lỗi khi người dùng biên dịch sang tài liệu. (lỗi gì nhỉ ?)

Đối với lớp tài liệu là `beamer`, các lệnh `\chapter`,  `\paragraph`,  `\subparagraph` không thể được thực thi. 

Một số lớp tài liệu như `minimal`, `letter` được thiết kế cho các mục đích rất tối giản, do đó chúng loại bỏ hầu hết hoặc toàn bộ các lệnh phân cấp. (? đoạn này còn mơ hồ quá, rốt cuộc nếu bỏ hầu hết thì còn những gì ? nếu vậy thì bỏ đoạn toàn bộ các lệnh phân cấp . . .)

Các tiêu đề được viết trong các lệnh phân cấp này sẽ được hệ thống hoàn toàn tự động đánh số ở trước nó như trong ví dụ sau đây đối với lớp tài liệu là `book`: 

```latex
\documentclass{book}
\usepackage[utf8]{vietnam}

\begin{document}

\part{Đây là phần I}  % Lớp book mặc định đánh số Phần bằng chữ số La Mã (Phần I, Phần II,...)

\chapter{Đây là chương đầu tiên} % Lớp book tự động thêm chữ "Chương 1" vào trước tiêu đề này

\section{Giới thiệu tổng quan} % Sẽ được tự động đánh số là: 1.1 Giới thiệu tổng quan
Đây là nội dung của mục đầu tiên.

\subsection{Tiểu mục chi tiết 1} % Sẽ được tự động đánh số là: 1.1.1 Tiểu mục chi tiết 1
Đây là nội dung của tiểu mục đầu tiên.

\subsection{Tiểu mục chi tiết 2} % Sẽ được tự động đánh số là: 1.1.2 Tiểu mục chi tiết 2
Đây là nội dung của tiểu mục thứ hai.


\section{Nội dung chính} % Sẽ được tự động đánh số là: 1.2 Nội dung chính
Đây là mục thứ hai trong Chương 1.


\chapter{Đây là chương thứ hai} % Hệ thống tự động nhảy sang "Chương 2"

\section{Phương pháp nghiên cứu} % Vì thuộc Chương 2 nên mục này sẽ tự động được đánh số là: 2.1 Phương pháp nghiên cứu
Đây là mục đầu tiên của chương 2.

\end{document}
```

Nếu như người dùng không muốn các tiêu đề trước nó được đánh số, người dùng chỉ cần thêm dấu `*` vào trong giữa lệnh phân cấp và dấu ngoặc nhọn `{}` của lệnh đó. 

Để dễ hình dung, ta quay lại với ví dụ ở trên. Nếu như người dùng thêm dấu `*` vào giữa lệnh `\section` và dấu ngoặc nhọn đang chứa tiêu đề là "Phương pháp nghiên cứu" 

```latex
\documentclass{book}
\usepackage[utf8]{vietnam}

\begin{document}

\part{Đây là phần I}  % Lớp book mặc định đánh số Phần bằng chữ số La Mã (Phần I, Phần II,...)

\chapter{Đây là chương đầu tiên} % Lớp book tự động thêm chữ "Chương 1" vào trước tiêu đề này

\section{Giới thiệu tổng quan} % Sẽ được tự động đánh số là: 1.1 Giới thiệu tổng quan
Đây là nội dung của mục đầu tiên.

\subsection{Tiểu mục chi tiết 1} % Sẽ được tự động đánh số là: 1.1.1 Tiểu mục chi tiết 1
Đây là nội dung của tiểu mục đầu tiên.

\subsection{Tiểu mục chi tiết 2} % Sẽ được tự động đánh số là: 1.1.2 Tiểu mục chi tiết 2
Đây là nội dung của tiểu mục thứ hai.


\section{Nội dung chính} % Sẽ được tự động đánh số là: 1.2 Nội dung chính
Đây là mục thứ hai trong Chương 1.


\chapter{Đây là chương thứ hai} % Hệ thống tự động nhảy sang "Chương 2"

\section*{Phương pháp nghiên cứu} % Có dấu * nên mục này sẽ KHÔNG được đánh số (Unnumbered section) và KHÔNG xuất hiện trong Mục lục.
Đây là mục đầu tiên của chương 2 nhưng không có số thứ tự phía trước.

\end{document}
```

thì tiêu đề của mục "Phương pháp nghiên cứu" ở chương 2, sẽ chỉ hiển thị chữ **"Phương pháp nghiên cứu"** mà không có số `2.1` ở phía trước như trong đoạn mã trước đó. 

---


 ki## Mục lục (Table of Contents)

Để tạo mục lục trong tài liệu đối với một số lớp tài liệu có thể được sử dụng [lệnh phân cấp](), người sử dụng lệnh 

```latex
\tableofcontents 
```

được đặt bên trong môi trường `document` và ngay sau lệnh `\maketitle`.

Ta lấy lại đoạn mã ví dụ ở bài học [lệnh phân cấp]() và thêm lệnh `\tableofcontents` vào trong đoạn mã đó. 

```latex
\documentclass{book}
\usepackage[utf8]{vietnam}

\begin{document}

\tableofcontents % Mục lục 

\part{Đây là phần I} 
% Lớp book mặc định đánh số Phần bằng chữ số La Mã (Phần I, Phần II,...)

\chapter{Đây là chương đầu tiên}
% Lớp book tự động thêm chữ "Chương 1" vào trước tiêu đề này

\section{Giới thiệu tổng quan}
% Sẽ được tự động đánh số là: 1.1 Giới thiệu tổng quan
Đây là nội dung của mục đầu tiên.

\subsection{Tiểu mục chi tiết 1}
% Sẽ được tự động đánh số là: 1.1.1 Tiểu mục chi tiết 1
Đây là nội dung của tiểu mục đầu tiên.

\subsection{Tiểu mục chi tiết 2}
% Sẽ được tự động đánh số là: 1.1.2 Tiểu mục chi tiết 2
Đây là nội dung của tiểu mục thứ hai.


\section{Nội dung chính}
% Sẽ được tự động đánh số là: 1.2 Nội dung chính
Đây là mục thứ hai trong Chương 1.


\chapter{Đây là chương thứ hai}
% Hệ thống tự động nhảy sang "Chương 2"

\section*{Phương pháp nghiên cứu}
% Có dấu * nên mục này sẽ KHÔNG được đánh số (Unnumbered section) và KHÔNG xuất hiện trong Mục lục.
Đây là mục đầu tiên của chương 2 nhưng không có số thứ tự phía trước.

\end{document}
```

Ta thấy các tiêu đề được đặt trong lệnh phân cấp đều hiển thị ở trong phần mục lục, chỉ riêng `\section*{Phương pháp nghiên cứu}` là không xuất hiện ở đó.  

Để thêm mục không đánh số (Unnumbered section) vào mục lục, người dùng sử dụng lệnh sau:

```latex
\addcontentsline{toc}{section}{Tiêu đề của phần}
```

. . . . (?)

Nếu như tiêu đề người dùng viết quá dài, chúng sẽ bị . . . khi xuất hiện ở phần mục lục như trong ví dụ dưới đây: 

```latex
\documentclass{article}

% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[utf8]{vietnam}

\begin{document}

\tableofcontents

\section{Tiêu đề phần nội dung này rất là dài và cần rút gọn bớt khi hiển thị trong mục lục}

\end{document}
```

Để khắc phục vấn đề này, người dùng chỉ cần viết một tiêu đề gọn lại ở trong dấu ngoặc vuông `[]` . . .  Áp dụng điều này vào lại ví dụ trên:  

```latex
\documentclass{article}

% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[utf8]{vietnam}

\begin{document}

\tableofcontents

\section[Tiêu đề rút ngọn]{Tiêu đề phần nội dung này rất là dài và cần rút gọn bớt khi hiển thị trong mục lục}

\end{document}
```

Người dùng có thể thấy tiêu đề ở ví dụ . . . đã được rút ngắn, gọn gàng lại khi hiện ở phần mục lục trong trang tài liệu.   

---
## Danh sách: 

Danh sách trong LaTeX bao gồm: danh sách không có thứ tự, danh sách có thứ tự và danh sách mô tả. 
### a. Danh sách không có thứ tự: 

Đối với danh sách không có thứ tự ta có lệnh sau: 

```latex
\begin{itemize} % môi trương danh sách không có thứ tự
    \item . . . % Liệt kê 
\end{itemize}
```

Ví dụ về danh sách không có thứ tự về các loại danh sách có trong LaTeX: 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}
\begin{itemize} 
    \item Danh sách không có thứ tự
    \item Danh sách có thứ tự
    \item Danh sách mô tả
\end{itemize}
\end{document}
```
### b. Danh sách có thứ tự: 

Danh sách có thứ tự trong LaTeX là danh sách được liệt kê theo thứ tự mặc định từ 1 đến số lượng danh sách cuối cùng được đưa ra: 

```latex
\begin{enumerate} % môi trường danh sách có thứ tự mặc định 
    \item . . . % liệt kê 
\end{enumerate}
```

Ví dụ về danh sách có thứ tự về các loại danh sách có trong LaTeX: 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}
Liệt kê các loại danh sách phổ biến trong \LaTeX{} bằng môi trường \verb|enumerate|
\begin{enumerate} 
    \item Danh sách không có thứ tự
    \item Danh sách có thứ tự
    \item Danh sách mô tả
\end{enumerate}
\end{document}
```

Nếu người dùng muốn sử dụng các . . . (`\item`) khác với mặc định mà LaTeX đưa ra, chẳng hạn thay vì liệt kê với số thứ tự mặc định từ 1 đến số lượng danh sách cuối cùng được đưa ra, người dùng cũng có thể liệt kê với số thứ tự theo kiểu chữ số La Mã là I, II, III, $\dots vv \dots$ hoặc cũng có thể được thay bằng chữ cái thường hoặc in hoa. 

Để làm được điều trên, người dùng chỉ cần thêm dấu `[]` bên cạnh `\item` của môi trường danh sách có thứ tự và đặt bên trong đó là kí hiệu mà người dùng muốn thay đổi sẽ xuất hiện ở đầu mỗi phần liệt kê của danh sách này: 

```latex
\begin{enumerate} % môi trường danh sách có thứ tự
    \item[thay đổi tại đây] . . . % liệt kê
\end{enumerate}
```

Đối với các chữ cái Hy Lạp cổ đại như $\alpha, \beta, ..vv..$ hay kí hiệu toán học (xem ở phần [toán học]()), người dùng cần đặt chúng vào bên trong một cặp dấu đô la đơn  `$...$`  và cặp dấu đô la đơn này sẽ được đặt ở bên trong dấu ngoặc vuông `[]`.

Ví dụ về danh sách có thứ tự với `\item` được kí hiệu theo chữ các Hy Lạp cổ đại về các loại danh sách có trong LaTeX: 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}
\begin{enumerate} 
    \item[$\alpha$] Danh sách không có thứ tự
    \item[$\beta$] Danh sách có thứ tự
    \item[$\gamma$] Danh sách mô tả
\end{enumerate}
\end{document}
```

### c. Danh sách lồng nhau:

Đối với các dang sách lồng vào nhau, người dùng chỉ cần thêm một danh sách con vào phần `\item` của môi trường danh sách cha đang sử dụng. 

Chẳng hạn ta có thể lồng danh sách có thứ tự mặc định của LaTeX vào các `item` của danh sách cha là danh sách không có thứ tự : 
```latex
\begin{itemize} % danh sách cha không có thứ tự  
    \item . . . % liệt kê
    \begin{enumerate} % danh sách con có thứ tự mặc định của LaTeX 
            \item . . . % liệt kê   
        \end{enumerate}
    \item . . . % liệt kê 
\end{itemize}
```

Ví dụ về . . . 
```latex

```

### d. Danh sách mô tả: 

Danh sách mô tả dùng để . . . 

Để tạo danh sách mô tả trong LaTeX, người dùng cần sử dụng môi trường `description` với lệnh sau: 
```latex
\begin{description} 
\item[Từ khóa 1] Mô tả hoặc giải thích cho từ khóa 1. 
\item[Từ khóa 2] Mô tả hoặc giải thích cho từ khóa 2. 
\item[Từ khóa 3] Mô tả hoặc giải thích cho từ khóa 3. 
\end{description}
```

--- 

## Liên kết thông thường:

Đầu tiên người dùng cần phải khai báo package sau:
```latex
\usepackage{hyperref}
```

Người dùng có thể thêm liên kết đến địa chỉ web vào phần soạn thảo LaTeX bằng cách **trực tiếp** hoặc **gián tiếp** sau.

### a. Chèn liên kết trực tiếp:

Sử dụng lệnh sau:

```latex
\url{<my_url>}
```

URL sẽ được hiển thị bằng phông chữ đơn cách ([monosaced font]), và nếu người dùng nhấp vào đó, trình duyệt web sẽ mở ra và trỏ đến đúng URL mà người dùng chèn vào lệnh.

Nếu như người dùng không thích để URL hiển thị với phông chữ đơn cách và muốn chúng được in với cùng kiểu chữ với phần còn lại của văn bản, người dùng có thể sử dụng lệnh sau:
```latex
\urlstyle{same}
```

Ví dụ đối với cách chèn link trực tiếp:

```latex
\documentclass{article} 
% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[english]{babel}
% Useful packages
\usepackage{hyperref} % 
\urlstyle{same} % 
% 
\title{Your Paper} 
\author{You}
\date{\today}
\begin{document}
\maketitle
\url{<https://github.com/Namlete102/LaTeX-Library-project-1.0.0>} % 
\end{document}
```

### b. Chèn liên kết gián tiếp:

Sử dụng lệnh sau:

```latex
\href{<my_url>}{description}
```

Nó sẽ hiển thị phần `description` bằng phông chữ chuẩn của tài liệu khi soạn. Khi người dùng nhấp vào phần `description` đó trên tài liệu, trình duyệt web sẽ mở ra và trỏ đến đúng URL bên trong `<my_url>` mà người dùng đã dùng để chèn vào lệnh trên.

Ví dụ:
```latex
\href{<https://github.com/Namlete/LaTeX-Library-project>}{Thư viện LaTeX}
```

Cả hai cách **trực tiếp** hoặc **gián tiếp** trên đều cùng trỏ đến trang của trình duyệt web. Nhưng với cách **trực tiếp**, thì URL sẽ được hiển thị trực tiếp ngay trên tài liệu. Trong khi cách **gián tiếp** thì URL sẽ bị ẩn, thay vào đó là chỉ hiển thị `description` mà người dùng đã chèn URL vào.

Ngoài việc có thể được sử dụng để chèn liên kết đến các trang web bằng phương pháp **gián tiếp** trên, lệnh `\href` có thể được sử dụng để cung cấp đến các **liên kết địa chỉ email**, **liên kết tệp nội bộ,** **liên kết đến bất kỳ đâu trong tệp PDF đầu ra ,v**à cũng như là **chèn liên kết thủ công (Inserting links manually).**

#### b.1. Liên kết địa chỉ email:

Sử dụng lệnh sau:
```latex
\href{mailto: <my_email>}{<my_email>}
```

Ví dụ:
```latex
\href{mailto: nguyenlenam15082007@gmail.com}{nguyenlenam15082007@gmail.com}
```

. . .

Xem lại tại đây: 
https://www.overleaf.com/learn/latex/Hyperlinks#Styles_and_colours 

--- 
## Siêu liên kết văn bản:

Để sử dụng siêu liên kết văn bản, người dùng cần phải khai báo package đã nêu ở bài học **Liên kết thông thường** trong phần soạn thảo LaTeX.

Package `hyperref` sẽ đảm nhiệm việc chuyển các **tham chiếu** trong tài liệu thành siêu liên kết.

Các thiết lập mặc định của LaTeX thường phù hợp với hầu hết người dùng. Cụ thể, nếu người dùng chỉ cần khai báo package `hyperref` là xong, mà không cần các thiết lập nào nữa khác, thì LaTeX sẽ chỉ kích hoạt ứng dụng mặc định của gói đó là siêu liên kết các tham chiếu và hiển thị các khung $\color{red}{\text{màu đỏ}}$ đối với [mục lục]() hoặc cũng có thể là [chú thích](), 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img2.1.jpg"
         alt="khung màu đỏ (mục lục) khi siêu liên kết văn">
	<figcaption>Ảnh lụm được ở <a href="https://tex.stackexchange.com/questions/528673/what-are-the-coloured-rectangles-in-research-papers">LaTeX Stack Exchange</a>. </figcaption>
</figure>

khung $\color{cyan}{\text{màu xanh dương}}$ đối với [liên kết thông thường](), 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img2.2.jpg"
         alt="khung màu xanh dương (mục lục) khi siêu liên kết văn">
    <figcaption>Ảnh lụm được ở <a href="https://tex.stackexchange.com/questions/528673/what-are-the-coloured-rectangles-in-research-papers">LaTeX Stack Exchange</a>. </figcaption>
</figure>

và khung $\color{green}{\text{màu xanh lá}}$ đối với [tài liệu tham khảo](), 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img2.3.jpg"
         alt="Khung màu xanh lá">
	<figcaption>Ảnh lụm được ở <a href="https://tex.stackexchange.com/questions/528673/what-are-the-coloured-rectangles-in-research-papers">LaTeX Stack Exchange</a>.</figcaption>
</figure>

Các khung hiện <font color="red">màu đỏ</font>, <font color="lightblue">màu xanh dương</font>, <font color="lightgreen">màu xanh lá</font> như vậy chỉ có trong tài liệu lúc người dùng vẫn còn làm việc ở trong phần soạn thảo LaTeX, giúp người dùng dễ dàng điều hướng. Các khung đó sẽ không còn xuất hiện ở trang tài liệu của người dùng khi tải về đề in. 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img2.4.jpg"
         alt="Khung màu sẽ biến mất khi tải tệp">
	<figcaption>Ảnh lụm được ở . . . .</figcaption>
</figure>

Nhưng nếu người dùng muốn thay đổi, chẳng hạn màu sắc của đường link sẽ bị thay đổi khi di chuột qua hoặc thay đổi màu sắc của đường link $\dots vv \dots$ , thì điều này cũng hoàn toàn có thể.

Bằng cách sử dụng lệnh:

```latex
\hypersetup{
    variable_name = new_value,
}
```

trong đó:
- `variable_name`: Là thuộc tính cấu hình do gói `hyperref` định nghĩa sẵn để điều khiển cách hoạt động hoặc hiển thị của các liên kết.
- `new_value`: Là giá trị bạn muốn gán cho thuộc tính đó để thay đổi thiết lập mặc định.

Người dùng có thể truyền `variable_name = new_value` vào `\hypersetup` bao nhiêu tùy thích, tùy thuộc vào kinh nghiệm của người dùng. Nên nhớ, hãy phân tách giữa các tên biến (`variable_name`) khác nhau bằng dấu phẩy, khi người dùng sử dụng chúng để thiết lập cho siêu liên kết văn bản. 

| **`variable_name`** | **`new_value`** | **Nhận xét**                                                                                                          |
| ------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------- |
| bookmarks           | = true, false   | Hiển thị (true) hoặc ẩn (false) cửa sổ Bookmark khi hiển thị tài liệu                                                 |
| unicode             | = true, false   | Có (true) hay không (false) cho phép sử dụng kí tự không có trong ngôn ngữ gốc Latin trong phần bookmarks của Acrobat |
| pdftoolbar          | = true,false    | Hiển thị (true) hay ẩn (false) thanh công cụ của Acrobat khi xem.                                                     |
| pdfmenubar          | = true,false    | Hiển thị (true) hay ẩn (false) thanh menu của Acrobat.                                                                |
|                     |                 |                                                                                                                       |

Để giúp người dùng tùy chỉnh nhanh hơn, đi cùng với đó là kết hợp với phần tham khảo bảng trên để theo dõi. Dưới đây sẽ là đoạn mã lệnh các biến với giá trị mặc định của chúng. Sao chép đoạn này vào trang soạn thảo tài liệu LaTeX và thực hiện các thay đổi, tùy ý của người dùng. Bên cạnh các tên biến và giá trị của biến đó là kèm theo dòng giải thích ngắn gọn về ý nghĩa của chúng. 

```latex
\hypersetup {
    bookmarks = true,          % hiển thị thanh dấu trang?
    unicode = false,           % ký tự không phải Latinh trong dấu trang của Acrobat
    pdftoolbar = true,         % hiển thị thanh công cụ của Acrobat?
    pdfmenubar = true,         % hiển thị menu của Acrobat?
    pdffitwindow = false,      % cửa sổ vừa với trang khi mở
    pdfstartview = {FitH} ,     % vừa chiều rộng của trang với cửa sổ
    pdftitle = {My title} ,     % tiêu đề
    pdfauthor = {Author} ,      % tác giả
    pdfsubject = {Subject} ,    % chủ đề của tài liệu
    pdfcreator = {Creator} ,    % người tạo tài liệu
    pdfproducer = {Produce} , % nhà sản xuất tài liệu
    pdfkeywords = {keyword1, key2, key3} , % danh sách từ khóa
    pdfnewwindow =true,       % liên kết trong cửa sổ PDF mới
    colorlinks = false,        % false: liên kết được đóng khung; true: liên kết có màu
    linkcolor = red,           % màu của các liên kết nội bộ (thay đổi màu khung bằng linkbordercolor)
    citecolor = green,         % màu của các liên kết đến thư mục tham khảo
    filecolor = cyan,          % màu của các liên kết tệp
    urlcolor = magenta,         % màu của các liên kết bên ngoài
}
```

Nếu người dùng không cần tùy chỉnh quá nhiều, sau đây lại là một vài ví dụ nhỏ nhưng hữu ích về việc tùy chỉnh siêu liên kết bằng các `variable_name` một cách đơn giản, hiệu quả cao mà người dùng có thể tham khảo.

Ví dụ: Khi xuất file PDF để in, các liên kết có màu không phải là lựa chọn tốt vì chúng sẽ bị chuyển thành màu xám trong bản in cuối cùng, gây khó đọc. Bằng cách sử dụng đoạn mã sau:

```latex
\usepackage{hyperref}
\hypersetup{
	colorlinks = false,
}
```

Hoặc cũng có thể làm cho các siêu liên kết đều có màu đen:

```latex
\usepackage{hyperref}
\hypersetup{
	links = black,
}
```

Ví dụ: Các liên kết trong phần soạn thảo LaTeX được tạo ra, tùy chỉnh dựa trên định dạng tài liệu sẽ đọc ở định dạng PDF. Tệp PDF có thể được tùy chỉnh để bổ sung thêm thông tin và thay đổi cách trình xem PDF hiển thị.

```latex
\hypersetup {
    colorlinks = true,
    linkcolor = blue,
    filecolor = magenta,
    urlcolor = cyan,
    pdftitle = {Overleaf Example}, % Tiêu đề của tập tin PDF đầu ra
    pdfpagemode = FullScreen,
}
```

<div align="center">

<img src="./images/img2.5.jpg">

</div>

. . . (còn nữa mà chưa soạn xem thêm dưới đây:  
https://en.wikibooks.org/wiki/LaTeX/Hyperlinks#Hyperlink_and_Hypertarget) 

---
## Các vấn đề với đường link:[^4]


---
## Chèn ảnh: [^10]

LaTeX không thể tự quản lý hình ảnh, vì vậy đầu tiên chúng ta cần sử dụng gói graphicx. Để sử dụng nó, người dùng cần thêm lệnh sau vào phần mở đầu:[^9]

```latex
\usepackage{graphicx}
```

. . . . 

```latex
\includegraphics[...]{...}
```

trong đó: 
+ Dấu ngoặc nhọn `{}` là nơi chứa hình ảnh mà người dùng muốn chèn vào tài liệu
+ Dấu ngoặc vuông `[]` là nơi mà người dùng tùy chọn (`option`) thay đổi kích thước của ảnh được chèn vào tài liệu.  
. . . 

Để canh ảnh phải hoặc trái ở lệnh `includegraphics` 

môi trường hình ảnh 

```latex
\begin{figure}[t]
\centering
\includegraphics[...]{...}
\caption{}
\label{}
\end{figure}
```

Người dùng có thể để lệnh `\caption` lên trước lệnh `\includegraphics` trong môi trường `figure` nếu muốn ghi caption trước hình ảnh 

```latex
\begin{figure}[t]
\centering
\caption{}
\includegraphics[...]{...}
\label{}
\end{figure}
```

. . . 

Để chèn nhiều hình ảnh vào cùng trong trang tài liệu, đầu tiên người dùng cần khai báo package sau:

```latex
\usepackage{subcaption}
```

sau đó người dùng sử dụng môi trường 

```latex
\begin{subfigure}{0.5\textwidth}
\includegraphics[width=0.9\linewidth, height=6cm]{mesh}
\caption{Caption 2}
\label{fig:subim2}
\end{subfigure}
```
được chèn vào trong môi trường `figure`. 

Mỗi một môi trường `subfigure` trong môi trường `figure` là một hình ảnh, ghi chú, canh chỉnh trái, phải ban đầu riêng biệt. 

. . . 

Hình ảnh được bao quanh bởi văn bản 

```latex
\begin{wrapfigure}{l}{0.25\textwidth}
    \centering
    \includegraphics[width=0.25\textwidth]{contour}
    \caption{Caption}
\end{wrapfigure}
```

Nhãn ở lệnh `label{}` trong môi trường `figure` cũng như môi trường `wrapfigure` và tham chiếu chéo đến hình ảnh bằng lệnh `\ref{}` . . . 

Với việc các caption được ghi ở lệnh `caption` trong các môi trường chèn hình ảnh trên, tài liệu LaTeX có khả năng tự động tạo danh sách hình ảnh nhờ vào lệnh sau:  

```latex
\listoffigures
```

. . .

---

## Chèn bảng

. . . 

--- 

## Chèn code:

Có hai kiểu chèn code bao gồm: `inline code` và `block code`. Trong đó: 
+ `inline code` là: 
+ `block code` là: 

### Inline code

Sử dụng lệnh sau:

```latex
\verb|. . .|
```


. . . 

---

## Chú thích (footnote) [^3]

Để chú thích ý nghĩa hoặc thông tin thêm cho một từ/cụm từ nào đó trong LaTeX, người dùng chỉ cần đặt lệnh 

```latex
\footnote{văn bản chú thích}
```

vào ngay sau từ mà người dùng cần được chú thích.  

Từ/cụm từ được chú thích sẽ xuất hiện thêm ở sau nó một chỉ số nhỏ nằm ở phía trên. Chỉ số này sẽ được hệ thống tự động thêm, cập nhật theo theo thứ tự tăng dần với các số mặc định là $1, 2, 3 \dots$, tương ứng với số lượng chú thích có trong trang tài liệu. 

Phần nội dung chú thích bên trong dấu ngoặc nhọn `{}` của lệnh `\footnote` sẽ được tự động hiển thị ở chân trang tài liệu hiện tại, có chỉ số nhỏ hiện thị ở trước phần nội dung đó sao cho tương ứng với chỉ số nhỏ hiển thị của từ/cụm từ được chú thích. 

Dưới đây là ví dụ về việc chú thích nhà vật lý Coulomb:

```latex
\documentclass[11pt]{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document} 
Phương trình toán học mô tả lực tương tác tĩnh điện giữa hai điện tích điểm trong chân không, được tìm thấy bởi nhà vật lý Coulomb\footnote{Charles-Augustin de Coulomb (1736 - 1806) là một sĩ quan, kỹ sư và nhà vật lý người Pháp, nổi tiếng với định luật mang tên ông là định luật Coulomb và ông còn được được đặt cho đơn vị SI đo điện tích (kí hiệu là C)}  
\[
F = k_e \frac{|q_1 q_2|}{r^2}
\]
\end{document}
```

<div align="center">

<img src="./images/Coulomb.jpg" alt="Coulomb">

Nhà vật lý người Pháp Charles-Augustin de Coulomb

</div>

> [!NOTE] 
> Người viết khuyên người dùng nên viết lệnh `\footnote` dính liền ngay sau từ cần chú thích, không nên để khoảng trắng ở giữa, vì điều này giúp chỉ số nhỏ hiển thị ở phía trên từ đó không bị nhảy hàng lỗi khi từ đó nằm ở cuối dòng văn bản. 

Trong trường hợp người dùng muốn tự quyết định chỉ số hiển thị của chú thích theo ý muốn của người, thay vì để LaTeX tự động đánh số $1, 2, 3 \dots$, người dùng có thể để `option` từ lệnh

```latex
\footnote[số thứ tự mới]{văn bản chú thích}
```

vào bên trong dấu ngoặc `[]` với bất kỳ số nguyên nào được nhập từ bàn phím. 

Áp dụng điều này vào lại ví dụ trên ta có

```latex
\documentclass[11pt]{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

% --- Các gói hỗ trợ toán học ---
\usepackage{amssymb} 
\usepackage{amsmath}

\begin{document} 

Phương trình toán học mô tả lực tương tác tĩnh điện giữa hai điện tích điểm trong chân không, được tìm thấy và chứng minh bởi nhà vật lý Coulomb\footnote[42]{Charles-Augustin de Coulomb (1736 - 1806) là nhà vật lý người Pháp, nổi tiếng với định luật mang tên ông là định luật Coulomb}: 

\[
F = k_e \frac{|q_1 q_2|}{r^2}
\]

\end{document}
```

Lúc này, trên trang tài liệu, người dùng có thể thấy rằng từ "Coulomb" lúc này mang chỉ số nhỏ hiển thị phía trên là **42**, còn ở chân trang phần nội dung chú thích của từ "Coulomb" cũng sẽ bắt đầu bằng số **42**.

---

## Toán học: [^5] [^7]

#### Giới thiệu:

Một trong những động lực lớn nhất thúc đẩy [Donald Knuth]() khi bắt đầu phát triển hệ thống TeX ban đầu là tạo ra một công cụ cho phép xây dựng các công thức toán học một cách đơn giản, đồng thời trông chuyên nghiệp khi in ấn. Việc ông thành công có lẽ là lý do tại sao TeX (và sau này là LaTeX) trở nên phổ biến trong cộng đồng khoa học. Việc trình bày toán học là một trong những thế mạnh lớn nhất của LaTeX. Đây cũng là một chủ đề rộng lớn do sự tồn tại của rất nhiều ký hiệu toán học.[^6] 

. . . . (viết tiếp)

---
#### `inline math`, `display math`: 

LaTeX cung cấp đầy đủ hai chế độ trình bày toán học chính bao gồm: 
+ `inline math`(**toán học nội tuyến**): được sử dụng để viết các biểu thức, kí hiệu toán học nằm trong một đoạn văn.
+ `display math`(**toán học hiển thị**): được sử dụng để viết các biểu thức, kí hiệu toán học không thuộc đoạn văn và được trình bày trên các dòng riêng biệt. 
##### `inline math`:

Để viết toán học ở chế độ `inline math`, người dùng cần viết chúng vào bên trong một trong ba cách sau:

1. Cặp dấu đô la đơn:`$...$`
2. Cặp dấu ngoặc tròn  `\(...\)`
3. Môi trường toán học (`math`)

```latex
\begin{math} 
. . . 
\end{math}
```

Điều này có nghĩa là người dùng có thể viết `inline math` phương trình toán học nổi tiếng từ định lý Pytago về mối quan hệ giữa hai cạnh góc vuông và một cạnh huyền trong một tam giác vuông bằng cặp dấu đô la đơn

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
Phương trình định lý Pytago: $x^2 + y^2 =z^2$
\end{document}
```

hoặc cũng có thể là bằng cặp dấu ngoặc tròn

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
Phương trình định lý Pytago: \(x^2 + y^2 =z^2\)
\end{document}
```

hay cũng thể là bằng môi trường `math`

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
\begin{math} 
Phương trình định lý Pytago: x^2 + y^2 =z^2
\end{math}
\end{document}
```

mà kết quả cho ra được đều sẽ là giống nhau: 

Phương trình định lý Pytago:  $x^2 + y^2 =z^2$ 

<div align="center">
<img src="./images/Pythagoras.jpg" alt="Pythagoras">
<p>Triết gia và nhà toán học người Hy Lạp cổ đại xứ Samos Pythagoras</p>
</div>

Việc lựa chọn một trong ba cách trên để viết `inline math` tùy thuộc vào sở thích, thói quen cá nhân của người dùng. 

> [!WARNING]  
> Nếu như người dùng không viết các dấu gạch dưới `_`, dấu mũ `^` và các [kí hiệu, chữ cái toán học]() khác vào một trong ba cách viết `inline math` trên, thì hệ thống sẽ báo lỗi `! Missing $ inserted.`

Người dùng có thể thấy ở đoạn mã dưới đây, các dấu mũ không được viết vào trong chế độ `inline math` 

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
Phương trình định lý Pytago: x^2 + y^2 =z^2 
\end{document}
```

Chú ý trên cũng được áp dụng tương tự đối với việc người dùng viết toán học ở chế độ [display math](). 
##### `display math`:

Để viết toán học ở chế độ `display math`, người dùng cần viết chúng vào bên trong một trong ba cách sau:

1. Cặp dấu đô la kép: `$$...$$`
2. Cặp dấu ngoặc vuông: `\[...\]`
3. Môi trường `displaymath`: 

```latex
\begin{displaymath} 
. . . 
\end{displaymath}
```

Tương tự như `inline math`, tùy thuộc vào sở thích, thói quen cá nhân của người dùng để có thể chọn một trong ba cách trên để viết toán học ở chế `display math`, mà vẫn đảm bảo kết quả cho ra được vẫn là giống nhau. 

Ví dụ về việc viết toán học ở chế độ `display math` với phương trình logarit của một tích là tổng của logarit của các thừa số: 

+ Phương trình được viết bên trong `$$...$$`

```latex
\documentclass{article}
\begin{document} % Sử dụng cặp dấu $$ để viết phương trình logarit
$$\log_b{xy} = \log_b{x} + \log_b{y}$$
\end{document}
```

+  Phương trình được viết bên trong `\[...\]`

```latex
\documentclass{article} % Sử dụng cặp dấu \[\] để viết phương trình logarit
\begin{document}
\[\log_b{xy} = \log_b{x} + \log_b{y}\] 
\end{document}
```

+  Phương trình được viết bên trong môi trường `displaymath`: 

```latex
\documentclass{article}
\begin{document}
\begin{displaymath} % Sử dụng môi trường displaymath để viết phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y}\
\end{displaymath}s
\end{document}
```

Kết quả cho ra được từ ba cách trên đều sẽ là giống hệt nhau

$$
\log_b{xy} = \log_b{x} + \log_b{y}
$$

<div align="center"> 

<img src="./images/John Napier.jpg" alt="John Napier">

Nhà toán học người Scotland John Napier

</div>

Trong một số trường hợp, khi người dùng viết tài liệu toán học cần [tham chiếu]() từ đoạn văn này đến phương trình toán học ở chế độ `display math`, mà không cần phải viết lặp lại, cũng như sẽ bị tràn ra khỏi văn bản đối với các [phương trình dài]() (? của phương trình đó ở chế độ `inline math` . . . (? viết tiếp đê)    

Khác với ba cách ở trên khi người dùng viết toán học ở chế độ `display math`, nếu như người dùng thay các cặp dấu, môi trường `displaymath` ở ví dụ . . . trên bằng một môi trường mới là môi trường `equation`, thì người dùng có thể thấy rằng phần toán học được đặt bên trong môi trường `equation` đó sẽ được LaTeX tự động đánh thêm một số thứ tự nằm bên phải phần toán học đó ở trong trang tài liệu.  

```latex
\documentclass{article}
\begin{document}
\begin{equation} % Sử dụng môi trường equation để đánh số thứ tự ở phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}
\end{document}
```

Kết quả cho ra được lúc này sẽ là: 

$$
\begin{equation}
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}
$$

Trong một số tài liệu toán học, đôi khi người dùng cũng thế thấy rằng số thứ tự được đánh bên cạnh phần toán học đó nằm ở bên trái thay vì bên phải như ở hình dưới đây

<div align="center"> 

<img src="./images/Kakeya.jpg" alt="John Napier">

Ảnh được cắt từ trang 1 bài báo toán học ["A STREAMLINED PROOF OF THE KAKEYA SET CONJECTURE IN $\mathbb{R^3}$](https://drive.google.com/file/d/1dlpgd5Q5AAOsaCFQK5MGRisJNUPmgxFu/view?usp=sharing) của ba nhà toán học [Larry Guth](https://math.mit.edu/~lguth/), [Hong Wang](https://sites.google.com/view/hongwang/home), [Joshua Zahl](https://jzahl.github.io/")

</div>

(? ảnh ba nhà toán học trên)

Để chuyển số thứ tự nằm từ bên phải sang bên trái như mặc định trên, người dùng chỉ cần thêm options

```latex
leqno
```

ở phần khai báo lớp tài liệu (`\documentclass`). 

```latex
\documentclass[leqno]{article} % 
\begin{document}
\begin{equation} % Sử dụng môi trường equation để đánh số thứ tự ở phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}
\end{document}
```

Để tham chiếu chéo đến phương trình toán học đó, người dùng cần sử dụng lệnh 

```latex
\label{} 
```

được đặt ở trong môi trường `equation`. 

Và lệnh 

```latex
\ref{}
```

hoặc lệnh 

```latex
\eqref{}
```

được đặt ở trong đoạn văn mà người dùng muốn để được tham chiếu đến phương trình có lệnh `\label` tương ứng.  

> [!NOTE]  
>  Nếu như người dùng để nội dung bên trong dấu ngoặc nhọn `{}` của lệnh `\ref`, cũng như là lệnh `\eqref` khác với nội dung bên trong dấu ngoặc nhọn của lệnh `\label`, thì hệ thống sẽ báo lỗi `Undefined reference` và ở trong trang tài liệu lệnh `\ref` (hoặc lệnh `\eqref` sẽ xuất hiện hai lần dấu chấm hỏi `??`. Vậy nên, nội dung bên trong dấu ngoặc nhọn của lệnh `\label` và lệnh `\ref` (hoặc `\eqref`) đều phải được giống hệt nhau. 

```latex
\documentclass{article}
\begin{document}
\begin{equation} % Sử dụng môi trường equation để đánh số thứ tự ở phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y}
\label{eq:1}
\end{equation}

. . . \ref{eq:2} . . .\ref{eq:1}

\end{document}
```

> [!NOTE]  
> Nếu như người dùng để nội dung bên trong dấu ngoặc nhọn `{}` của nhiều lệnh `\label` là giống hệt nhau thì hệ thống sẽ báo lỗi `multiply-defined labels`. Hơn nữa, nếu `\label` bị trùng nội dung với nhau, thì  lệnh `\ref` cũng như là lệnh `\eqref` sẽ được hệ thống mặc định trỏ đến nhãn ở vị trí có `\label` xuất hiện gần nhất.  Vậy nên, nội dung bên trong dấu ngoặc nhọn của mỗi lệnh `\label` là phải khác nhau.  

```latex
\documentclass{article}

\begin{document}

\begin{equation} % 
\log_b{xy} = \log_b{x} + \log_b{y}
\label{eq:1} % 
\end{equation}

\begin{equation} % 
\log_b{\frac{x}{y}} = \log_b{x} - \log_b{y} 
\label{eq:1} % 
\end{equation}

. . . \ref{eq:1} . . . 

\end{document}
```

Hai chú ý trên cũng được áp dụng tương tự với các bài học [hình ảnh](), [bảng](), ..vv..   

Điểm khác biệt của lệnh `\ref` và `\eqref` đó là lệnh `\eqref` sẽ tự động đóng ngoặc tròn `()` số thứ tự tương ứng với phương trình được tham chiếu, còn lệnh `\ref` thì không. Để dễ hình dung, người dùng xem qua đoạn mã sau đây   

```latex
\documentclass{article}
\begin{document}
\begin{equation} % Sử dụng môi trường equation để đánh số thứ tự ở phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y}
\label{eq:1} % . . .
\end{equation}

. . . (\ref{eq:1}) % lệnh \ref không được hệ thống tự động đóng ngoặc tròn, mà người dùng phải tự chủ động thêm vào nếu cần.    
. . . \eqref{eq:1} % lệnh \eqref được hệ thống tự động đóng ngoặc tròn, mà người dùng không cần phải tự chủ động thêm vào. 

\end{document}
```

Nếu như người dùng không muốn xuất hiện số thứ tự bên cạnh phần toán học khi viết phần toán học đó bằng môi trường `equation`, thì người dùng có thể quay lại ba cách đầu tiên mà người viết đã hướng dẫn khi viết toán học ở chế độ [`display math`](), hoặc người dùng cũng có thể sử dụng một cách mới sau.  

Trước tiên người dùng cần phải khai báo package sau

```latex
\usepackage{amsmath}
```

Package `amsmath` còn cung cấp cho người dùng một số tùy chọn để sắp xếp và hiển thị bố cục phương trình toán học sao cho phù hợp với tài liệu người dùng, ngay cả khi các phương trình rất dài hoặc nếu người dùng phải đưa nhiều phương trình vào cùng một dòng, để tránh việc viết phương trình có thể thiếu tính linh hoạt, dẫn đến việc chồng chéo hoặc thậm chí cắt bớt một phần phương trình khi nó quá dài [?].  

. . . (*viết sau*) https://www.overleaf.com/learn/latex/Aligning_equations_with_amsmath

Tiếp đến, người dùng chỉ cần thêm dấu `*` vào bên trong dấu ngoặc nhọn `{}` của lệnh môi trường `equation` là phương trình logarit ở ví dụ . . . sẽ không còn xuất hiện số thứ tự bên cạnh ở trong trang tài liệu nữa:  

```latex
\documentclass{article}
\begin{document}
\begin{equation*} % Sử dụng môi trường equation* để viết phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation*}
\end{document}
```

Kết quả lúc này ta nhận được giống với ba cách đầu tiên trên: 

$$
\log_b{xy} = \log_b{x} + \log_b{y}
$$

Việc thêm dấu `*` như trên cũng được áp dụng tương tự đối với các môi trường khác như môi trường `aligned` (xem ở bài học . . .), . . . (viết tiếp)  

**(?)** Điểm khác biệt của môi trường `equation*` và `displaymath` là gì ? Nên sử dụng chúng trong trường hợp nào ? (xem qua issues đây https://github.com/Namlete102/LaTeX-Library-project/issues/1) 

> [!NOTE]
> Khi người dùng viết toán học dù ở chế độ `inline math` hay `display math`, người dùng không được phép để các biểu thức,  toán tử, kí hiệu, chữ cái toán học có các khoảng trống ở mỗi dòng. Nếu không, thì hệ thống sẽ báo lỗi  `Missing $ inserted`

Để dễ hình dung lưu ý trên, người dùng hãy xem qua ví dụ sau đây với phương trình Clapeyron-Mendeleev thiết lập mối liên hệ giữa các đại lượng áp suất, thể tích, và nhiệt độ của một khối khí lý tưởng: 

```latex
\documentclass{article}
\begin{document}
\[
P \cdot V 

= n \cdot T \cdot R
\]
\end{document}
```

Có thể thấy ở đoạn mã trên, nếu người dùng vô tình để khoảng trống giữa các dòng biểu thức $P \cdot V$  và $= n \cdot T \cdot R$, thì hệ thống sẽ lập tức báo lỗi `Missing $ inserted`:  

Ta khắc phục lỗi ở đoạn mã ở ví dụ . . . bằng cách xóa đi khoảng trắng giữa hai biểu thức đó

```latex
\documentclass{article}
\begin{document}
\[
P \cdot V 
= n \cdot T \cdot R
\]
\end{document}
```

hoặc thêm [chú thích]() vào khoảng trống giữa hai biểu thức đó

```latex
\documentclass{article}
\begin{document}
\[
P \cdot V 
% Điều này sẽ loại bỏ dòng trống
= n \cdot T \cdot R
\]
\end{document}
```

mà kết quả cho ra được đều sẽ là như sau

$$P \cdot V = n \cdot T \cdot R$$

<div align="center">

<img src="./images/Clapeyron-Mendeleev.jpg" alt="Clapeyron-Mendeleev">

Nhà vật lý người Pháp Émile Clapeyron (Bên trái) và nhà hóa học người Nga Dmitry Mendeleev (Bên phải) (Ảnh lụm được đâu đó trên mạng)

</div>

---
### Kí hiệu, chữ cái toán học  (? đặt tên lại)

Để viết kí hiệu, chữ cái toán học ở chế độ là `inline math`, cũng như là `display math`, người dùng chỉ cần viết chúng ở bên trong các các cặp kí hiệu, môi trường mà người viết đã trình bày ở [`inline math`, `display math`](). 

Ví dụ về công thức tính định thức tổng quát của một ma trân vuông $A$ cấp $n$ được chứng minh bởi nhà toán học Leibniz  

```latex
\documentclass{article}
\begin{document}
\[
\mathrm{det}(A) = \sum_{\sigma \in S_n} sgn(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )
\]
\end{document}
```

Người dùng có thể thấy, trong công thức tính định thức của Leibniz có chữ cái Hy Lạp là $\sigma$ (đọc là sigma) được dùng để quy ước về khái niệm phép thế (?) trong lĩnh vực đại số của toán học. 

$$
    \mathrm{det}(A) = \sum_{\sigma \in S_n} sgn(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )
$$

<div align="center">

<img src="./images/Leibniz.jpg" alt="Leibniz">

Triết gia, nhà toán học người Đức Gottfried Wilhelm Leibniz

</div>

Người dùng có thể tham khảo thêm ở [danh sách các kí hiệu toán học, chữ cái Hy Lạp](), nếu như người dùng chưa biết hoặc là quên cách ghi các kí hiệu, chữ cái toán học trong lúc thực hành soạn thảo LaTeX. 

Một số yếu tố toán học cần được trình bày bằng các kiểu phông chữ khác chẳng hạn các ký tự/ký hiệu theo một kiểu nhất định, khác nhau khi trình bày toán học. [^14] (?)

Ví dụ, người dùng có thể viết kí hiệu toán học của các tập số theo kiểu chữ đậm bảng đen (?) như tập các số tự nhiên $\mathbb{N}$, tập các số nguyên $\mathbb{Z}$, tập các số thực $\mathbb{R}$, $\dots vv \dots$ 

<div align="center">

<img src="./images/Setnumber.jpg" alt="Hành tím">

Ảnh lụm được ở <a href="https://www.facebook.com/photo.php?fbid=488758739928398&set=pb.100063828282373.-2207520000&type=3">Mathtasy Toán học thú vị</a>

</div>

Để viết được các kiểu phông chữ khác nhau dành cho kí hiệu toán học, trước tiên người dùng cần phải khai báo package sau: 

```latex
\usepackage{amssymb}
```

Package `amssymb` . . . 

Để viết được phông chữ các kí hiệu về tập số ở ví dụ trên, người dùng cần để chữ cái thường đó vào lệnh

```latex
\mathbb{}
```

Với kí hiệu tập số tự nhiên ta viết như sau 

```latex
\documentclass{article}
\usepackage{amssymb}
\begin{document}
$\mathbb{N}$
\end{document}
```

Người dùng có thể đọc thêm [các kiểu phông chữ khác nhau dành cho kí hiệu toán học]() đây để tham khảo. 

https://www.overleaf.com/learn/latex/Mathematical_fonts 

---
### Dấu ngoặc: [^1]  

Dấu ngoặc rất phổ biến trong việc bao quát các biểu thức, toán tử trong toán học. Một số dấu ngoặc thông dụng được sử dụng, đi kèm với lệnh của chúng trong LaTeX được trình bày ở bảng dưới đây: 

|      Ký hiệu      | Tên tiếng Việt                      | Tên tiếng Anh                     | Lệnh LaTeX                                             |
| :---------------: | :---------------------------------- | :-------------------------------- | :----------------------------------------------------- |
|       $( )$       | Dấu ngoặc đơn                       | Parentheses (or Round brackets)   | `(...)` (nhập dấu ngoặc tròn trên bàn phím)            |
|       $[ ]$       | Dấu ngoặc vuông                     | Brackets (or Square brackets)     | `[...]` (nhập dấu ngoặc vuông trên bàn phím)           |
|      $\{ \}$      | Dấu ngoặc nhọn                      | Braces (or Curly brackets)        | `\{...\}` (nhập dấu ngoặc nhọn trên bàn phím)          |
| $\langle \rangle$ | Dấu ngoặc nhọn góc / Ngoặc nhọn dẹt | Angle brackets                    | `\langle ... \rangle`                                  |
|   $\vert \vert$   | Dấu trị tuyệt đối / Dấu gạch đứng   | Vertical bars (or Absolute value) | `\vert...\vert` hoặc `\|...\|` (nhập \| trên bàn phím) |
|   $\Vert \Vert$   | Dấu chuẩn (Toán học) / Dấu gạch đôi | Double vertical bars (or Norm)    | `\Vert...\Vert` hoặc `\|\| ...\|\|`                    |
| $\lfloor \rfloor$ | Dấu hàm sàn / Ngoặc dưới            | Floor brackets                    | `\lfloor...\rfloor`                                    |
|  $\lceil \rceil$  | Dấu hàm trần / Ngoặc trên           | Ceiling brackets                  | `\lceil...\rceil`                                      |
|                   |                                     |                                   |                                                        |

Để viết toán học ở chế độ `inline math` hoặc `display math` được bao quát bởi dấu ngoặc, người dùng chỉ cần đặt phần toán học đó vào bên trong các dấu ngoặc ở bảng trên một cách bình thường. 

Ví dụ về phần toán học được đặt trong dấu ngoặc tròn với công thức De Moivre dùng để nâng một số phức dưới dạng lượng giác lên lũy thừa bậc $n$ một cách nhanh chóng.

```latex
\documentclass{article}
\begin{document}
\[( \cos \theta + i\sin \theta )^n = \cos n \theta + i\sin n \theta\]
\end{document}
```

Kết quả cho ra được sẽ là

$$
( \cos \theta + i\sin \theta )^n = \cos n \theta + i\sin n \theta 
$$

<div align="center">

<img src="./images/Abraham de Moivre.jpg" alt="Moivre">

Nhà toán học người Pháp Abraham de Moivre

</div>

Bên cạnh đó, người dùng cần lưu tâm đến một số lưu ý quan trọng sau đây khi sử dụng dấu ngoặc trong LaTeX. 

#### 1. Quy tắc tự động thay đổi kích thước (Auto-resizing)

Nếu công thức bên trong dấu ngoặc có chứa phân số ($\frac{a}{b}$), dấu tích phân ($\int$) hoặc số mũ cao ($a^x$) , các dấu ngoặc thông thường sẽ bị quá nhỏ và mất cân đối. Để dấu ngoặc tự động co giãn và bao quát trọn vẹn phần công thức bên trong, người dùng hãy thêm lệnh `\left` và `\right` vào ngay trước dấu ngoặc tương ứng.

Ví dụ về phương trình Friedmann thứ nhất . . . : 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[ 
\text{H}^2 = \left( \frac{\dot{a}}{a} \right)^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
\]
\end{document}
```

Kết quả cho ra được sẽ là: 

$$
\text{H}^2 = \left( \frac{\dot{a}}{a} \right)^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
$$

Nếu như người dùng không thêm lệnh `\left` và `\right` vào mỗi bên trước dấu ngoặc như ở ví dụ trên 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
% . . . 
\[ 
\text{H}^2 = (\frac{\dot{a}}{a})^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
\] 
\end{document}
```

Kết quả lúc này cho ra được sẽ là: 

$$
\text{H}^2 = (\frac{\dot{a}}{a})^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
$$

Người dùng có thể thấy, dấu ngoặc tròn `()` ở mỗi bên phân số $\dfrac{\dot{a}}{a}$ không được tự điều chỉnh kích thước sao cho phù hợp với kích thước của phân số đó. 

<div align="center">

<img src="./images/Friedmann.jpg" alt="Friedmann">

Nhà vũ trụ học và nhà toán học người Nga Alexander Friedmann

</div>

#### 2. Nguyên tắc hiển thị dấu ngoặc nhọn `\{ \}`

Trong cú pháp của LaTeX, ngoặc nhọn `{..}` được mặc định sử dụng để nhóm các tham số hoặc tập lệnh lại với nhau nên không hiển thị khi xuất bản trang tài liệu.  Do đó, để hiển thị được dấu ngoặc nhọn hiển thị ra trang tài liệu, người dùng bắt buộc cần phải thêm dấu gạch chéo ngược `\` mà người viết đề cập ở bài học [kí tự đặc biệt]() vào ngay trước chúng.

Ví dụ điều này với tích Descartes của hai tập hợp $A$ và $B$, kí hiệu là $A \times B$ là tập hợp của các cặp $(a,b)$ trong đó $a \in A$, $b \in B$ theo thứ tự $a$ trước $b$ sau:

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
A \times B = \{(a,b)|a \in A, b \in B\}
\]
\end{document}
```

Kết quả nhận được từ ví dụ trên sẽ là: 

$$
A \times B = \{ \ (a,b) \ | \ a \ \in \ A, \ b \ \in \ B\}
$$

<div align="center">

<img src="./images/Rene Descartes.jpg" alt="Descartes">

Nhà toán học và triết gia người Pháp René Descartes

</div>

#### 3. Cú pháp dấu ngoặc một bên 

Trong nhiều trường hợp viết toán học như biểu diễn hệ phương trình, điều kiện xét hàm số,  $\dots vv \dots$ , người dùng sẽ cần một dấu ngoặc lớn mở ở bên trái nhưng lại không có ở bên phải. Hoặc ngược lại là người dùng sẽ cần một dấu ngoặc lớn mở ở bên phải nhưng lại không có ở bên trái như khi gom nhiều điều kiện giả thiết độc lập trong chứng minh hình học/đại số để suy ra một kết luận chung, hoặc khi định nghĩa hàm số phân nhánh theo chiều ngược $\dots vv \dots$

Để xử lý cấu trúc này, người dùng vẫn sẽ dùng cặp lệnh `\left` và `\right`, nhưng ở phía không cần hiển thị dấu ngoặc nhọn, người dùng hãy thay ký hiệu dấu ngoặc bằng một dấu chấm `.` 

Trường hợp 1 với việc hiển thị dấu ngoặc lớn mở ở bên trái nhưng không có ở bên phải ta có:

```latex
\left \{

\right.
```

Trường hợp 2 với việc hiển thị dấu ngoặc lớn mở ở bên phải nhưng không có ở bên trái ta có:

```latex
\left.

\right \}
```


Và bên trong lệnh của cả hai trường hợp đó, người dùng cần thêm môi trường `matrix` sau
```latex
\begin{matrix} 
. . . 
\end{matrix}
```

Ví dụ . . .  với dãy số Fibonacci được xác định bởi hệ thức truy hồi tuyến tính 

```latex
\documentclass{article}
\begin{document}
\[
\left\{
    \begin{matrix}
		u_1 = 1 \\ 
		u_2 = 1 \\ 
		u_{n+1} = u_n + u_{n-1}, \forall n \geq 2  
    \end{matrix}
\right.
\]
\end{document}
```

Kết quả cho ra được sẽ chỉ xuất hiện một dấu ngoặc nhọn lớn duy nhất che phủ ở bên trái của .  .  . 

$$
\begin{cases}
u_1 = 1 \\ 
u_2 = 1 \\ 
u_{n} = u_{n-1} + u_{n-2}, \ \forall n \geq 3  
\end{cases}
$$

Hoặc người dùng cũng có thể sử dụng môi trường `cases` sau:

```latex
\begin{cases}
. . .
\end{cases}
```

Viết lại ví dụ . . . trên bằng môi trường `cases`: 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{cases} % không cần phải thêm môi trường matrix 
	u_1 = 1 \\ 
	u_2 = 1 \\ 
	u_{n+1} = u_n + u_{n-1}, \forall n \geq 2  
\end{cases}
\]
\end{document}
```

Kết quả cho ra được vẫn sẽ tương tự với kết quả ta có được ở trên. 

<div align="center">

<img src="./images/Fibonacci.jpg" alt="Fibonacci">

Nhà toán học người Ý Fibonacci

</div>


. . . (viết tiếp ví dụ với dấu ngoặc lớn hiển thị ở bên phải mà ko có ở bên trái)

Tham khảo: https://gemini.google.com/app/4475fd095760fba9?hl=vi 

--- 

### Chỉ số trên và chỉ số dưới: 

Để viết chỉ số trên người dùng sử dụng kí hiệu `^`, còn với chỉ số dưới người dùng sử dụng kí hiệu `_` . 

Các kí hiệu chỉ số trên và chỉ số dưới được đặt ở sau kí hiệu, chữ cái toán học. 

Ví dụ về chỉ số trên với phương trình từ định lý cuối cùng của Fermat được chứng minh bởi nhà toán học Andrew Wiles 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
x^n + y^n = z^n, \forall x,y,z, n \in \mathbb{Z^+}, n > 2
\]
\end{document}
```

Kết quả cho ra được sẽ là:

$$
x^n + y^n = z^n, \forall x,y,z, n \in \mathbb{Z^+}, n > 2
$$

<div align="center">

<img src="./images/Andrew Wiles.jpg" alt="Andrew Wiles">

Nhà toán học người Anh Andrew Wiles

</div>

Ví dụ về chỉ số dưới với phương trình entropy của nhà vật lý Boltzmann thể hiện mối quan hệ giữa entropy và số cách sắp xếp các nguyên tử hoặc phân tử của một hệ nhiệt động nhất định [^2]

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[S = k_b \cdot \Omega\]
\end{document}
```

Kết quả cho ra được sẽ là:

$$
S = k_b \cdot \Omega 
$$

<div align="center">

<img src="./images/Boltzmann.jpg" alt="Ludwig Boltzmann">

Nhà vật lý người Áo Ludwig Boltzmann

</div>

Các kí hiệu chỉ số trên và chỉ số dưới cũng có thể được kết hợp trong cùng một biểu thức $C^k_n$ (đọc là tổ hợp chập $k$ của $n$ phần tử) như ở ví dụ về công thức nhị thức Newton giúp khai triển lũy thừa bậc nguyên dương của một tổng thành tổng các đơn thức 

```latex
\documentclass{article}
\begin{document}
\[
(a + b)^n = C^k_n a^{n-k} b^k
\]
\end{document}
```

Kết quả nhận được sẽ là 

$$
(a + b)^n = C^k_n a^{n-k} b^k
$$

<div align="center">

<img src="./images/Isaac Newton.jpg" alt="I.Newton">

Nhà vật lý người Anh Isaac Newton

</div>

Cũng ở ví dụ về công thức nhị thức Newton trên, người dùng có thể thấy để viết được biểu thức dài $n-k$ ở chỉ số trên của $a$, chúng cần được gom lại trong dấu ngoặc nhọn `{}` được đặt sau kí hiệu chỉ số trên.

Điều này cũng được áp dụng tương tự đối với chỉ số dưới. 

Ví dụ . . . với phương trình trường hấp dẫn Einstein mô tả trọng lực không phải là một lực kéo thông thường theo quan điểm vật lý cổ điển của nhà vật lý Isaac Newton, mà là hệ quả của sự uốn cong không-thời gian do khối lượng và năng lượng . . .  gây ra.  

```latex
\documentclass{article}
\begin{document}
\[
R_{\mu\nu} - \frac{1}{2}g_{\mu\nu}R + g_{\mu\nu}\Lambda = \frac{8\pi G}{c^4}T_{\mu\nu} 
\] 
\end{document}
```

$$
R_{\mu\nu} - \frac{1}{2}g_{\mu\nu}R + g_{\mu\nu}\Lambda = \frac{8\pi G}{c^4}T_{\mu\nu} 
$$

Người dùng có thể thấy, để viết được bao quát chỉ số dưới $\mu\nu$, chúng cần được viết vào trong bởi dấu ngoặc `{}`. 

<div align="center">

<img src="./images/Albert Einstein.jpg" alt="Einstein">

Nhà vật lý người Đức Albert Einstein

</div>

---

### Viết văn bản trong chế độ toán học 

Khi viết văn bản trong toán học, chẳng hạn . . . (nên viết lại thành một vấn đề ví dụ mới)

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\begin{document}
\[
Văn bản trong toán học
\]
\end{document}
```

Kết quả cho ra được là các từ sẽ được in nghiêng và bị dính vào nhau

$$
Văn bản trong toán học 
$$

Để viết được văn bản trong toán học, người dùng cần sử dụng lệnh `\text{}` để ngăn cách phần toán học với phần văn bản.  

Áp dụng lại điều này ở ví dụ trên ta có

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\begin{document}
\[
\text{Văn bản trong toán học}
\]
\end{document}
```

Kết quả lúc này sẽ khác hoàn toàn so với khi chưa thêm văn bản vào trong lệnh `\text{}`

$$
\text{Văn bản trong toán học}
$$

---

### Khoảng cách trong chế độ toán học:  [^12]

Khi người dùng viết toán học,  . . . (nêu vấn đề)

Để điều chỉnh khoảng cách giữa các biểu thức, toán tử . . . người dùng chỉ cần thêm lệnh ở bảng sau đây 

| Lệnh LaTeX | Mô tả                                                   | Ví dụ         |
| :--------- | :------------------------------------------------------ | ------------- |
| `\quad`    | = 18 mu                                                 | $a \quad b$   |
| `\qquad`   | $= 2 \cdot$`\quad` (= 36 mu)                            | $a \qquad b$  |
| `\enskip`  | $= \frac{1}{2} \cdot$`\quad` (= 9 mu)                   | $a \enskip b$ |
| `\,`       | $= \frac{3}{18} \cdot$`\quad` (= 3 mu)                  | $a \, b$      |
| `\:`       | $= \frac{4}{18} \cdot$`\quad` (= 4 mu)                  | $a \: b$      |
| `\;`       | $= \frac{5}{18} \cdot$`\quad` (= 5 mu)                  | $a \; b$      |
| `\!`       | $= \frac{-3}{18} \cdot$`\quad` (= -3 mu)                | $a \! b$      |
| `\`        | tương đương với khoảng trắng trong văn bản thông thường | $a \ b$       |

(Bảng tham khảo từ [Overleaf](https://www.overleaf.com/learn/latex/Spacing_in_math_mode)) 

vào ngay bên cạnh . . . 

Ví dụ về khoảng cách trong chế độ toán học với các biểu thức, toán tử trong định lý Taylor[^11]  . . . 

```latex
\documentclass{article}

\usepackage[utf8]{vietnam}

\begin{document}

\[
f(x) \ = \ f(a) \ + \ \frac{f'(a)}{1!}(x-a) \ + \ \frac{f^{''}(a)}{2!}(x-a)^2 \ + \ \frac{f^{'''}(a)}{3!}(x-a)^3 \ + \ \dots \  = \ \sum^\infty_{n = 0}\frac{f^{(n)}(a)}{n!}(x-a)^n 
\]

\end{document}
```

$$
f(x) \ = \ f(a) \ + \ \frac{f'(a)}{1!}(x-a) \ + \ \frac{f^{''}(a)}{2!}(x-a)^2 \ + \ \frac{f^{'''}(a)}{3!}(x-a)^3 \ + \ \dots \  = \ \sum^\infty_{n = 0}\frac{f^{(n)}(a)}{n!}(x-a)^n
$$


<div align="center">

<img src="./images/Brooks Taylor.jpg" alt="Taylor">

Nhà toán học người Anh Brooks Taylor

</div>

---
### Màu trong toán học[^15] 

(vì sao đôi khi ta cần màu trong công thức toán học ?) 

Để viết các kí hiệu toán học có màu, người dùng có thể sử dụng lệnh `\textcolor` ở bài học [màu chữ]() hoặc cũng có thể thay thế lệnh đó bằng lệnh sau

```latex
\mathcolor{color}{text}
```

Tương tự như lệnh `textcolor`, người dùng có thể sử dụng các màu khác nhau ngoài 19 màu cơ bản cũng đã nêu ở bài học [màu chữ]() cho lệnh `mathcolor`  

Ví dụ . . .  với công thức Euler về mối liên hệ giữa đỉnh, cạnh, mặt của khối đa diện lồi. Cụ thể, với mọi khối đa diện lồi nào, số đỉnh trừ đi số cạnh cộng với số mặt luôn cho ra kết quả là bằng 2: [^16]

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath} % for the equation* environment
\usepackage{xcolor} % for text color 

\begin{document}

\[\mathcolor{red}{V} - \mathcolor{blue}{E} + \mathcolor{green}{F} = 2\]

trong đó: 

\begin{itemize}
    \item \textcolor{red}{V}: Số đỉnh (Vertex) của khối đa diện lồi
    \item \textcolor{blue}{E}: Số cạnh (Edge) của khối đa diện lồi
    \item \textcolor{green}{F}: Số mặt phẳng (Face) của khối đa diện lồi
\end{itemize}
\end{document}
```

$$
\textcolor{red}{V} - \textcolor{blue}{E} + \textcolor{green}{F} = 2 
$$

<div align="center">

<img src="./images/Leonhard Euler.jpg" alt="Euler">

Nhà toán học người Thụy Sĩ Leonhard Euler

</div>

---

### Tiên đề, định nghĩa, định lý, định luật, mệnh đề, bổ đề, giả thiết, bằng chứng, hệ quả, ví dụ:[^19]

. . .  (Giới thiệu các định nghĩa trên ở phần sau cuốn sách)   

. . .  Để sử dụng được định nghĩa, . . . . (gồm những gì nữa) trước tiên người dùng cần khai báo ...(gì ?) 

```latex
\newtheorem{}{}
```

trong đó: 
+ (giải thích hai dấu ngoặc nhọn kia)
+ 

(? lệnh này được đặt ở đâu) 

Khi biên dịch sang trang tài liệu, các từ định nghĩa, định lý, ..vv.. sẽ được viết sang tiếng Anh. 

. . . (ví dụ với môi trường tiên đề về tiên đề Peano . . . trong đó từ tiên đề là tiếng Anh) 

```latex
\documentclass{article}
\newtheorem{axiom}{axiom} % for theorem vietnamese
\begin{document}
\begin{axiom}[Gauss - Wantzel]

\end{axiom}

\end{document}
```

Để viết các từ ấy sang tiếng Việt người dùng trước tiên cần nhớ phải khai báo package [viết tiếng Việt ](),  và sau đó đổi từ theorem (tiếng Anh) sang từ định lý (tiếng Việt), ..vv.. ở dấu ngoặc nhọn ngoài cùng của lệnh trên

. . . (ví dụ môi trường định nghĩa với từ định nghĩa là tiếng Việt) 

```latex
\newtheorem{theorem}{Định lý}
. . . 
\begin{theorem}
. . . 
\end{theorem}
```

Ví dụ về môi trường định lý với định lý Gauss - Wantzel và môi trường định nghĩa với định nghĩa về số nguyên tố Fermat, trong đó từ định lý và định nghĩa đều được viết sang tiếng Việt 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % for Vietnamese 
\newtheorem{theorem}{Định lý} % for theorem vietnamese
\newtheorem{definition}{Định nghĩa} % for difinition vietnamese
\begin{document}

\begin{theorem}[Gauss - Wantzel]
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

\begin{definition}[Số nguyên tố Fermat]
Số nguyên có dạng là 
\[
F_n = 2^{2^n}+1 
\]
nếu kết quả đầu ra tính được từ $F_n$ là một số nguyên tố, thì nó được gọi là số nguyên tố Fermat. 
\end{definition}

\end{document}
```
. . . 

(? Edit ảnh Gauss - Wantzel - Fermat)

Người dùng cũng có thể sử dụng lệnh . . . nhằm để tên . . . thay vì chỉ từ axioms thông thường như các ví dụ định lý, định nghĩa trên khi biên dịch sang trang tài liệu như ở ví dụ dưới đây về tiên đề Euclid cho nền tảng hình học sơ cấp, trong đó từ tiên đề được viết sang tiếng Việt  

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % for Vietnamese
\newtheorem{axiom}{Tiên đề Peano} % for theorem vietnamese
\begin{document}
\begin{axiom}
. . . (5 tiên đề Peano)
\end{axiom}
\end{document}
```

Cần phải đảm bảo rằng khi người dùng đã định nghĩa môi trường axiom thì từ "axiom" trong dấu ngoặc ở lệnh `\newtheorem` không được lặp lại lần nữa khi người dùng muốn sử dụng chúng để viết một tiên đề khác. 

Sẽ có . . . cách hiểu sau  

Nếu như người dùng sử dụng lại môi trường axiom, thì ở phần tiêu đề . . . vẫn sẽ xuất hiện "Tiên đề Peano": 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % for Vietnamese
\newtheorem{axiom}{Tiên đề Peano} % for theorem vietnamese
\begin{document}
\begin{axiom}
. . .  (tiên đề Hilbert)
\end{axiom}
\end{document}
```

Nếu như người dùng định nghĩa tiên đề . . . trùng với . . . thì hệ thống sẽ báo lỗi 

. . . 



. . . (không muốn có số thứ tự bên cạnh. . . ) 

Trước tiên người dùng cần phải khai báo package sau:

```latex
\usepackage{amsthm} % for theorem environments
```

. . . (giải thích đôi chút gói này) 

Sau đó người dùng chỉ cần thêm dấu `*` ở sau lệnh `\newtheorem` và trước hai dấu ngoặc nhọn (? mô tả hơi chán, nên viết lại sau)

```latex
\newtheorem*{}{}
```

Ví dụ về nhận xét không có đánh số (?). . . với . . . , trong đó từ nhận xét được viết sang tiếng Việt

```latex
\usepackage[utf8]{vietnam}
\usepackage{amsthm}
\newtheorem*{remark}{Nhận xét} 
. . .
\begin{remark}
. . .
\end{remark} 
```

(? Nêu vấn đề vì sao ta lại phải phân biệt định nghĩa, định lý) Nhằm phân biệt được định nghĩa, định lý, ..vv.. trong trang tài liệu toán học người dùng sử dụng lệnh

```latex
\theoremstyle{stylename}
```

trong đó **stylename** gồm các kiểu cơ bản mặc định của hệ thống được tổng hợp ở bảng sau:[^20]

| stylename  | Đặc điểm và công dụng                                                                                                                                                                                 | Ví dụ                                 |
| :--------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| definition | Tiêu đề in đậm, nội dung chữ thường. Được sử dùng trong định nghĩa, điều kiện, vấn đề và đưa ra ví dụ.                                                                                                | **Định nghĩa** 1: Nội dung định nghĩa |
| plain      | Tiêu đề in đậm, nội dung in nghiêng. Được sử dụng trong các định lý, bổ đề, hệ quả, mệnh đề và giả thuyết.                                                                                            | **Định lý 2**: *Nội dung định lý*     |
| remark     | Tiêu đề in nghiêng, nội dung in thường. Được sử dụng trong nhận xét, ghi chú, chú thích (notes), tuyên bố (annotations), trường hợp (claims), lời cảm ơn (acknowledgments) và kết luận (conclusions). | *Nhận xét 3*: Nội dung nhận xét       |

Ở mỗi kiểu **stylename** khác nhau, ta sẽ có những ví dụ khác nhau dưới đây để giúp người dùng dễ dàng hình dung để hiểu các lệnh trên rõ hơn. 

Ví dụ về stylename **definition** với vấn đề bài toán 

Ví dụ về stylename **plain** với bổ đề Bezout [^21]  trong đó từ bổ đề được viết sang tiếng Việt

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % for Vietnamese 
\usepackage{amssymb} 
\usepackage{amsthm}
\theoremstyle{plain} 
\newtheorem{lemma}{Bổ đề} % for lemma vietnamese
\begin{document}
\begin{lemma}
Cho $a, b \in \mathbb{Z}$ là hai số nguyên tố bất kì, luôn tồn tại $u, v \in \mathbb{Z}$ sao cho 
\[
a \cdot u + b \cdot v = d
\]
trong đó d = gcd(a,b) là ước chung lớn nhất của hai số a và b. 
\end{lemma}
\end{document}
```

<div align="center"> 

<img src="LaTeX-Library-project-v1.0.0/images/Bezout.jpg">

</div>

(Nhà toán học người Pháp Étienne Bézout. Nguồn ảnh: https://mathshistory.st-andrews.ac.uk/Biographies/Bezout/poster/lived/)

Ví dụ về stylename **remark** với . . .:

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % for Vietnamese 
\usepackage{amssymb} 
\usepackage{amsthm}
\theoremstyle{remark} 
\newtheorem*{}{} 
\begin{document}

\end{document}
```

Bằng chứng (tiếng anh là proof) là . . . 

Để viết bằng chứng trong LaTeX, người dùng sử dụng môi trường `proof`

Với môi trường `proof`, chúng đã được có trong sẵn package `amsthm` mà ta đã khai báo ở . . . (phần bài học nhân xét mà không đánh số ở trên) 

```latex
\begin{proof}
. . .
\begin{proof}
```

Ví dụ với chứng minh định lý $\sqrt{2}$ không là số hữu tỉ: 

```latex
. . . 
```

Khi kết thúc phần chứng minh cho định lý, mệnh đề, bổ đề, ..vv.. nào đó trong toán học, chúng ta luôn kết lại bằng câu "điều phải chứng minh".  Điều này bắt nguồn từ . . . được viết tắt ngắn gọn lại là QED[^18]  

. . . (Để sử dụng từ QED khi kết thúc chứng minh, người dùng sử dụng lệnh sau): 

```latex
\renewcommand\qedsymbol{QED}
```

Từ QED trên có thể được thay thế bằng một ô vuông đen

```latex
\renewcommand\qedsymbol{$\blacksquare$}
```

hoặc là một ô vuông trắng 

```latex
\renewcommand{\qedsymbol}{$\square$} 
```

Các lệnh trên đều phải được đặt trước môi trường `proof` như ở ví dụ đoạn mã sau đây  . . .

```latex
. . . 
```


---

### Các bài học toán khác 

Viết toán học luôn là chủ đề yêu thích của tác giả, vậy nên có lẽ sẽ hợp lý nếu như tác giả vừa giới thiệu phần chủ đề toán học, cũng như là cách viết các kí hiệu toán học đó trên LaTeX thì sẽ một công đôi việc, mang đến cảm giác thú vị đến người đọc.

<div align="center">

<img src="LaTeX-Library-project-v1.0.0/images/LoveMath.jpg">

Keep calm and love math

</div>

---

#### Liên phân số:  [^13]

Đối với một . . . 

---

#### Giới hạn, đạo hàm, tích phân: 

Đây là một chủ đề toán học thú vị được gọi chung là giải tích . . . 

Khi viết kí hiệu tổng . . .  nếu viết thông thường bằng lệnh `\sum` thì kết quả cho ra được là $\sum$ (đọc là sigma) 

Để thay đổi kích thước các kí hiệu toán học khi viết toán học ở chế độ `inline math` người dùng có thể sử dụng thêm bốn lệnh ở bảng sau đây: 

| Lệnh                 | Ví dụ                     | Kết quả từ ví dụ          |
| :------------------- | ------------------------- | ------------------------- |
| `\displaystyle`      | `\displaystyle(123)`      | $\displaystyle (123)$     |
| `\textstyle`         | `\textstyle(123)`         | $\textstyle (123)$        |
| `\scriptstyle`       | `\scriptstyle(123)`       | $\scriptstyle (123)$      |
| `\scriptscriptstyle` | `\scriptscriptstyle(123)` | $\scriptscriptstyle(123)$ |

vào trước lệnh `\sum` . . . kết quả cho ra được lúc này là $\displaystyle \sum$ 

. . . 

---

#### Vector, ma trận: 

(phương pháp biến đổi sơ cấp) 

---

#### Số phức:  

. . .

---

#### Thuật toán Euclid

. . . 


---

### Danh sách các kí hiệu toán học, chữ cái Hy Lạp

Tham khảo trang 70 tài liệu đây: **Một tài liệu ngắn gọn giới thiệu về LATEX 2ε - hay LATEX 2ε trong 155 phút**,  https://www.cmor-faculty.rice.edu/~heinken/latex/symbols.pdf cũng như là **LaTeX Formal Methods Reference**  https://www.cs.put.poznan.pl/ksiek/latexmath.html#id2

#### Các dấu trọng âm trong chế độ soạn thảo toán học: 

| Lệnh        | Kí hiệu     | Lệnh        | Kí hiệu     | Lệnh          | Kí hiệu       | Lệnh            | Kí hiệu         |
| :---------- | ----------- | ----------- | ----------- | ------------- | ------------- | --------------- | --------------- |
| `\hat{a}`   | $\hat{a}$   | `\check{a}` | $\check{a}$ | `\tilde{a}`   | $\tilde{a}$   | `\acute{a}`     | $\acute{a}$     |
| `\grave{a}` | $\grave{a}$ | `\dot{a}`   | $\dot{a}$   | `\ddot{a}`    | $\ddot{a}$    | `\breve{a}`     | $\breve{a}$     |
| `\bar{a}`   | $\bar{a}$   | `\vec{a}`   | $\vec{a}$   | `\widehat{A}` | $\widehat{A}$ | `\widetilde{A}` | $\widetilde{A}$ |

#### Các chữ cái Hy Lạp viết thường


![](LaTeX-Library-project-v1.0.0/images/img6.1.jpg)

(trang chú trang 57 từ tài liệu **Một tài liệu ngắn gọn giới thiệu về LATEX 2ε - hay LATEX 2ε trong 155 phút** 

| Lệnh     | Kí hiệu  | Lệnh        | Kí hiệu     | Lệnh     | Kí hiệu  | Lệnh       | Kí hiệu    |
| :------- | -------- | ----------- | ----------- | -------- | -------- | ---------- | ---------- |
| `\alpha` | $\alpha$ | `\theta`    | $\theta$    | `o`      | $o$      | `\upsilon` | $\upsilon$ |
| `\beta`  | $\beta$  | `\vartheta` | $\vartheta$ | `\pi`    | $\pi$    | `\phi`     | $\phi$     |
| `\gamma` | $\gamma$ | `\iota`     | $\iota$     | `\varpi` | $\varpi$ | `\varphi`  | $\varphi$  |
| `\delta` | $\delta$ | `\kappa`    | $\kappa$    | `\rho`   | $\rho$   | `\chi`     | $\chi$     |
|          |          |             |             |          |          |            |            |

. . . 


---

## Chèn tài liệu tham khảo: 



---
# b. Footnote 

[^1]: Nguồn tham khảo viết ở Overleaf: https://www.overleaf.com/learn/latex/Brackets_and_Parentheses 

[^2]: https://en.wikipedia.org/wiki/Boltzmann%27s_entropy_formula

[^3]: Nguồn tham khảo viết chú thích ở Overleaf: https://www.overleaf.com/learn/latex/Footnotes)

[^4]: Nguồn tham khảo viết các vấn đề siêu liên kết ở Overleaf: https://en.wikibooks.org/wiki/LaTeX/Hyperlinks#Troubleshooting

[^5]: Nguồn tham khảo viết toán học ở Overleaf: https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes#Adding_math_to_LaTeX. 

[^6]: https://en.wikibooks.org/wiki/LaTeX/Mathematics

[^7]: Nguồn tham khảo lời viết này sử dụng ở Wikibook: https://en.wikibooks.org/wiki/LaTeX/Mathematics

[^8]: Nguồn ảnh màu LaTeX: https://tex.stackexchange.com/questions/659029/colour-packages-beyond-xcolor 

[^9]: Nguồn tham khảo viết chèn hình ảnh ở Overleaf bao gồm: https://www.overleaf.com/learn/latex/Inserting_Images%23Positioning#Introduction; https://www.overleaf.com/learn/latex/Positioning_images_and_tables

[^10]: Nguồn tham khảo tử Overleaf: https://www.overleaf.com/learn/latex/Inserting_Images%23Positioning

[^11]: Công thức tham khảo từ: https://mathworld.wolfram.com/TaylorSeries.html 

[^12]: Tham khảo từ bài học Overleaf: https://www.overleaf.com/learn/latex/Spacing_in_math_mode

[^13]: Tham khảo từ bài tạp chí Epsilon: https://epsilonvn.github.io/archives/epsilon_vol01_2015February.pdf

[^14]: Tham khảo từ Overleaf: https://www.overleaf.com/learn/latex/Mathematical_fonts

[^15]: Tham khảo cuốn "How to Reproduce this Book Exactly with LaTeX A Self-contained Tutorial on Writing Mathematical Notes" trang 47. 

[^16]: Nguồn tài liệu tham khảo phần công thức Euler ở tạp chí Pi: https://drive.google.com/file/d/1O_QiD8GcipW0DXclsRH7HoWUsnr9pE4y/view?usp=sharing)

[^17]: Nguồn copy: https://en.wikipedia.org/wiki/Lorem_ipsum 

[^18]: Không nên nhầm lẫn với định nghĩa QED ở các lĩnh vực khác: https://en.wikipedia.org/wiki/QED

[^19]: Tham khảo viết từ: https://paulwintz.com/mathematical-writing/theorem-like-environments-in-latex/

[^20]: Nguồn viết: https://www.overleaf.com/learn/latex/Theorems_and_proofs#Reference_guide + https://en.wikibooks.org/wiki/LaTeX/Theorems#Theorem_styles

[^21]: Nguồn tham khảo viết: https://mathworld.wolfram.com/BezoutsTheorem.html
