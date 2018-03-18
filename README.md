# r-project-1

R version 3.4.3 (2017-11-30) -- "Kite-Eating Tree"
Copyright (C) 2017 The R Foundation for Statistical Computing
Platform: x86_64-w64-mingw32/x64 (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details.

R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications.

Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R.

[Workspace loaded from ~/.RData]

> chhh
       roll.no grade
1   15071A05G6  9.56
2   15071A05D9  9.53
3   15071A05E0  9.47
4   15071A05D5  9.43
5   15071A05C1  9.40
6   15071A05F3  9.40
7   15071A05G5  9.37
8   15071A05D6  9.34
9   15071A05C2  9.31
10  15071A05E6  9.31
11  15071A05E8  9.31
12  15071A05C4  9.29
13  15071A05E4  9.27
14  15071A05H1  9.25
15  15071A05G7  9.22
16  15071A05D0  9.18
17  15071A05D7  9.11
18  15071A05H2  9.11
19  15071A05F2  9.04
20  15071A05G1  8.99
21  15071A05F7  8.98
22  15071A05F5  8.97
23  15071A05D1  8.91
24  15071A05E1  8.89
25  15071A05G8  8.88
26  15071A05H7  8.85
27  15071A05G9  8.84
28  16075A0533  8.84
29  15071A05E5  8.83
30  15071A05G2  8.82
31  15071A05I0  8.82
32  15071A05D8  8.81
33  15071A05F0  8.81
34  15071A05F4  8.81
35  15071A05H0  8.76
36  15071A05H5  8.70
37  15071A05C9  8.54
38  15071A05F6  8.45
39  15071A05E3  8.44
40  15071A05G0  8.37
41  15071A05C6  8.31
42  15071A05G3  8.23
43  15071A05F8  8.05
44  15071A05D2  7.90
45  15071A05H4  7.79
46  15071A05H6  7.77
47  15071A05F1  7.51
48  16075A0525  7.50
49  16075A0530  7.50
50  16075A0529  7.40
51  15071A05H9  7.37
52  15071A05E7  7.33
53  16075A0536  7.30
54 14071A05C1`  7.24
55  15071A05H3  7.23
56  15071A05C7  7.00
57  15071A05H8  6.90
58  16075A0526  6.80
59  16075A0528  6.71
60  16075A0535  6.71
61  16075A0532  6.63
62  16075A0531  6.50
63  15071A05C5  6.44
64  15071A05C3  6.40
65  15071A05D3  6.25
66  15071A05C8  6.20
67  15071A05F9  6.16
68  15071A05D4  6.00
> 
> filter(chhh,grade>9.0)
Error in filter(chhh, grade > 9) : object 'grade' not found
In addition: Warning message:
In data.matrix(data) : NAs introduced by coercion
> filter(chhh,grade>"9.0")
Error in filter(chhh, grade > "9.0") : object 'grade' not found
In addition: Warning message:
In data.matrix(data) : NAs introduced by coercion
> filter(chhh,chh$grade>"9.0")
Time Series:
Start = 1 
End = 68 
Frequency = 1 
   [,1] [,2]
 1    0    0
 2    0    0
 3    0    0
 4    0    0
 5    0    0
 6    0    0
 7    0    0
 8    0    0
 9    0    0
10    0    0
11    0    0
12    0    0
13    0    0
14    0    0
15    0    0
16    0    0
17    0    0
18    0    0
19    0    0
20    0    0
21    0    0
22    0    0
23    0    0
24    0    0
25    0    0
26    0    0
27    0    0
28    0    0
29    0    0
30    0    0
31    0    0
32    0    0
33    0    0
34    0    0
35    0    0
36    0    0
37    0    0
38    0    0
39    0    0
40    0    0
41    0    0
42    0    0
43    0    0
44    0    0
45    0    0
46    0    0
47    0    0
48    0    0
49    0    0
50    0    0
51    0    0
52    0    0
53    0    0
54    0    0
55    0    0
56    0    0
57    0    0
58    0    0
59    0    0
60    0    0
61    0    0
62    0    0
63    0    0
64    0    0
65    0    0
66    0    0
67    0    0
68    0    0
Warning message:
In data.matrix(data) : NAs introduced by coercion
> class(chhh)
[1] "tbl_df"     "tbl"        "data.frame"
> filter(chhh,grade<9)
Error in filter(chhh, grade < 9) : object 'grade' not found
In addition: Warning message:
In data.matrix(data) : NAs introduced by coercion
> filter(chhh,grade == "9")
Error in filter(chhh, grade == "9") : object 'grade' not found
In addition: Warning message:
In data.matrix(data) : NAs introduced by coercion
> library(dplyr)

Attaching package: ‘dplyr’

The following objects are masked from ‘package:stats’:

    filter, lag

The following objects are masked from ‘package:base’:

    intersect, setdiff, setequal, union

> filter(chhh,grade == "9")
# A tibble: 0 x 2
# ... with 2 variables: roll.no <chr>, grade <dbl>
> filter(chhh,grade <= "9" & grade > 8)
# A tibble: 24 x 2
   roll.no    grade
   <chr>      <dbl>
 1 15071A05G1  8.99
 2 15071A05F7  8.98
 3 15071A05F5  8.97
 4 15071A05D1  8.91
 5 15071A05E1  8.89
 6 15071A05G8  8.88
 7 15071A05H7  8.85
 8 15071A05G9  8.84
 9 16075A0533  8.84
10 15071A05E5  8.83
# ... with 14 more rows
> great9<-filter(chhh,grade > "9")
> great9
# A tibble: 19 x 2
   roll.no    grade
   <chr>      <dbl>
 1 15071A05G6  9.56
 2 15071A05D9  9.53
 3 15071A05E0  9.47
 4 15071A05D5  9.43
 5 15071A05C1  9.40
 6 15071A05F3  9.40
 7 15071A05G5  9.37
 8 15071A05D6  9.34
 9 15071A05C2  9.31
10 15071A05E6  9.31
11 15071A05E8  9.31
12 15071A05C4  9.29
13 15071A05E4  9.27
14 15071A05H1  9.25
15 15071A05G7  9.22
16 15071A05D0  9.18
17 15071A05D7  9.11
18 15071A05H2  9.11
19 15071A05F2  9.04
> 
> bet8and9<-filter(chhh,grade >=8 & grade< 9 )
> bet8and9
# A tibble: 24 x 2
   roll.no    grade
   <chr>      <dbl>
 1 15071A05G1  8.99
 2 15071A05F7  8.98
 3 15071A05F5  8.97
 4 15071A05D1  8.91
 5 15071A05E1  8.89
 6 15071A05G8  8.88
 7 15071A05H7  8.85
 8 15071A05G9  8.84
 9 16075A0533  8.84
10 15071A05E5  8.83
# ... with 14 more rows
> bet8.5and9<-filter(chhh,grade >=8.5 & grade< 9 )
> bet8.5and9
# A tibble: 18 x 2
   roll.no    grade
   <chr>      <dbl>
 1 15071A05G1  8.99
 2 15071A05F7  8.98
 3 15071A05F5  8.97
 4 15071A05D1  8.91
 5 15071A05E1  8.89
 6 15071A05G8  8.88
 7 15071A05H7  8.85
 8 15071A05G9  8.84
 9 16075A0533  8.84
10 15071A05E5  8.83
11 15071A05G2  8.82
12 15071A05I0  8.82
13 15071A05D8  8.81
14 15071A05F0  8.81
15 15071A05F4  8.81
16 15071A05H0  8.76
17 15071A05H5  8.70
18 15071A05C9  8.54
> bet8.5and8<-filter(chhh,grade >=8 & grade< 8.5 )
> bet8.5and8
# A tibble: 6 x 2
  roll.no    grade
  <chr>      <dbl>
1 15071A05F6  8.45
2 15071A05E3  8.44
3 15071A05G0  8.37
4 15071A05C6  8.31
5 15071A05G3  8.23
6 15071A05F8  8.05
> less8<-filter(chhh,grade<8)
> less8
# A tibble: 25 x 2
   roll.no    grade
   <chr>      <dbl>
 1 15071A05D2  7.90
 2 15071A05H4  7.79
 3 15071A05H6  7.77
 4 15071A05F1  7.51
 5 16075A0525  7.50
 6 16075A0530  7.50
 7 16075A0529  7.40
 8 15071A05H9  7.37
 9 15071A05E7  7.33
10 16075A0536  7.30
# ... with 15 more rows
> groups<-rbind(less8,bet8.5and8)
> groups
# A tibble: 31 x 2
   roll.no    grade
   <chr>      <dbl>
 1 15071A05D2  7.90
 2 15071A05H4  7.79
 3 15071A05H6  7.77
 4 15071A05F1  7.51
 5 16075A0525  7.50
 6 16075A0530  7.50
 7 16075A0529  7.40
 8 15071A05H9  7.37
 9 15071A05E7  7.33
10 16075A0536  7.30
# ... with 21 more rows
> groups<-cbind(less8,bet8.5and8)
Error in data.frame(..., check.names = FALSE) : 
  arguments imply differing number of rows: 25, 6
> matrix(less8,bet8.5and8)
Error in matrix(less8, bet8.5and8) : non-numeric matrix extent
> matrix(less8,bet8.5and8,nrow=2,ncol = 3)
Error in matrix(less8, bet8.5and8, nrow = 2, ncol = 3) : 
  invalid 'byrow' argument
> matrix(less8,bet8.5and8,nrow=2,ncol = 3,byrow =TRUE)
Error in matrix(less8, bet8.5and8, nrow = 2, ncol = 3, byrow = TRUE) : 
  length of 'dimnames' [1] not equal to array extent
> matrix(less8,bet8.5and8,nrow=5,ncol = 7,byrow =TRUE)
Error in matrix(less8, bet8.5and8, nrow = 5, ncol = 7, byrow = TRUE) : 
  length of 'dimnames' [1] not equal to array extent
In addition: Warning message:
In matrix(less8, bet8.5and8, nrow = 5, ncol = 7, byrow = TRUE) :
  data length [2] is not a sub-multiple or multiple of the number of rows [5]
> matrix(less8,bet8.5and8,nrow=5,ncol = 6,byrow =TRUE)
Error in matrix(less8, bet8.5and8, nrow = 5, ncol = 6, byrow = TRUE) : 
  length of 'dimnames' [1] not equal to array extent
> array(less8,bet8.5and8)
Error in array(less8, bet8.5and8) : 
  (list) object cannot be coerced to type 'integer'
> install.packages(plyr)
Error in install.packages : object 'plyr' not found
> install.packages("plyr")
Installing package into ‘C:/Users/rahul/Documents/R/win-library/3.4’
(as ‘lib’ is unspecified)
trying URL 'https://cran.rstudio.com/bin/windows/contrib/3.4/plyr_1.8.4.zip'
Content type 'application/zip' length 1219389 bytes (1.2 MB)
downloaded 1.2 MB

package ‘plyr’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\rahul\AppData\Local\Temp\RtmpKkIIez\downloaded_packages
> library(plyr)
---------------------------------------------------------------------------------------------------------------
You have loaded plyr after dplyr - this is likely to cause problems.
If you need functions from both plyr and dplyr, please load plyr first, then dplyr:
library(plyr); library(dplyr)
---------------------------------------------------------------------------------------------------------------

Attaching package: ‘plyr’

The following objects are masked from ‘package:dplyr’:

    arrange, count, desc, failwith, id, mutate, rename, summarise, summarize

Warning message:
package ‘plyr’ was built under R version 3.4.4 
> cbind.fill(less8,bet8.5and8)
Error in cbind.fill(less8, bet8.5and8) : 
  could not find function "cbind.fill"
> rbind.fill(less8,bet8.5and8)
       roll.no grade
1   15071A05D2  7.90
2   15071A05H4  7.79
3   15071A05H6  7.77
4   15071A05F1  7.51
5   16075A0525  7.50
6   16075A0530  7.50
7   16075A0529  7.40
8   15071A05H9  7.37
9   15071A05E7  7.33
10  16075A0536  7.30
11 14071A05C1`  7.24
12  15071A05H3  7.23
13  15071A05C7  7.00
14  15071A05H8  6.90
15  16075A0526  6.80
16  16075A0528  6.71
17  16075A0535  6.71
18  16075A0532  6.63
19  16075A0531  6.50
20  15071A05C5  6.44
21  15071A05C3  6.40
22  15071A05D3  6.25
23  15071A05C8  6.20
24  15071A05F9  6.16
25  15071A05D4  6.00
26  15071A05F6  8.45
27  15071A05E3  8.44
28  15071A05G0  8.37
29  15071A05C6  8.31
30  15071A05G3  8.23
31  15071A05F8  8.05
> 
> merge(less8,bet8.5and8)
[1] roll.no grade  
<0 rows> (or 0-length row.names)
> merge(less8,bet8.5and8,all=TRUE)
       roll.no grade
1  14071A05C1`  7.24
2   15071A05C3  6.40
3   15071A05C5  6.44
4   15071A05C6  8.31
5   15071A05C7  7.00
6   15071A05C8  6.20
7   15071A05D2  7.90
8   15071A05D3  6.25
9   15071A05D4  6.00
10  15071A05E3  8.44
11  15071A05E7  7.33
12  15071A05F1  7.51
13  15071A05F6  8.45
14  15071A05F8  8.05
15  15071A05F9  6.16
16  15071A05G0  8.37
17  15071A05G3  8.23
18  15071A05H3  7.23
19  15071A05H4  7.79
20  15071A05H6  7.77
21  15071A05H8  6.90
22  15071A05H9  7.37
23  16075A0525  7.50
24  16075A0526  6.80
25  16075A0528  6.71
26  16075A0529  7.40
27  16075A0530  7.50
28  16075A0531  6.50
29  16075A0532  6.63
30  16075A0535  6.71
31  16075A0536  7.30
> library(rowr)
Error in library(rowr) : there is no package called ‘rowr’
> install.packages("rowr")
Installing package into ‘C:/Users/rahul/Documents/R/win-library/3.4’
(as ‘lib’ is unspecified)
trying URL 'https://cran.rstudio.com/bin/windows/contrib/3.4/rowr_1.1.3.zip'
Content type 'application/zip' length 31174 bytes (30 KB)
downloaded 30 KB

package ‘rowr’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\rahul\AppData\Local\Temp\RtmpKkIIez\downloaded_packages
> library(rowr)

Attaching package: ‘rowr’

The following object is masked from ‘package:plyr’:

    count

The following objects are masked from ‘package:dplyr’:

    coalesce, count

> Map(cbind.fill,less8,bet8.5and8)
$roll.no
        object     object
1   15071A05D2 15071A05F6
2   15071A05H4 15071A05E3
3   15071A05H6 15071A05G0
4   15071A05F1 15071A05C6
5   16075A0525 15071A05G3
6   16075A0530 15071A05F8
7   16075A0529 15071A05F6
8   15071A05H9 15071A05E3
9   15071A05E7 15071A05G0
10  16075A0536 15071A05C6
11 14071A05C1` 15071A05G3
12  15071A05H3 15071A05F8
13  15071A05C7 15071A05F6
14  15071A05H8 15071A05E3
15  16075A0526 15071A05G0
16  16075A0528 15071A05C6
17  16075A0535 15071A05G3
18  16075A0532 15071A05F8
19  16075A0531 15071A05F6
20  15071A05C5 15071A05E3
21  15071A05C3 15071A05G0
22  15071A05D3 15071A05C6
23  15071A05C8 15071A05G3
24  15071A05F9 15071A05F8
25  15071A05D4 15071A05F6

$grade
   object object
1    7.90   8.45
2    7.79   8.44
3    7.77   8.37
4    7.51   8.31
5    7.50   8.23
6    7.50   8.05
7    7.40   8.45
8    7.37   8.44
9    7.33   8.37
10   7.30   8.31
11   7.24   8.23
12   7.23   8.05
13   7.00   8.45
14   6.90   8.44
15   6.80   8.37
16   6.71   8.31
17   6.71   8.23
18   6.63   8.05
19   6.50   8.45
20   6.44   8.44
21   6.40   8.37
22   6.25   8.31
23   6.20   8.23
24   6.16   8.05
25   6.00   8.45

> Map(cbind.fill,less8,bet8and9)
$roll.no
        object     object
1   15071A05D2 15071A05G1
2   15071A05H4 15071A05F7
3   15071A05H6 15071A05F5
4   15071A05F1 15071A05D1
5   16075A0525 15071A05E1
6   16075A0530 15071A05G8
7   16075A0529 15071A05H7
8   15071A05H9 15071A05G9
9   15071A05E7 16075A0533
10  16075A0536 15071A05E5
11 14071A05C1` 15071A05G2
12  15071A05H3 15071A05I0
13  15071A05C7 15071A05D8
14  15071A05H8 15071A05F0
15  16075A0526 15071A05F4
16  16075A0528 15071A05H0
17  16075A0535 15071A05H5
18  16075A0532 15071A05C9
19  16075A0531 15071A05F6
20  15071A05C5 15071A05E3
21  15071A05C3 15071A05G0
22  15071A05D3 15071A05C6
23  15071A05C8 15071A05G3
24  15071A05F9 15071A05F8
25  15071A05D4 15071A05G1

$grade
   object object
1    7.90   8.99
2    7.79   8.98
3    7.77   8.97
4    7.51   8.91
5    7.50   8.89
6    7.50   8.88
7    7.40   8.85
8    7.37   8.84
9    7.33   8.84
10   7.30   8.83
11   7.24   8.82
12   7.23   8.82
13   7.00   8.81
14   6.90   8.81
15   6.80   8.81
16   6.71   8.76
17   6.71   8.70
18   6.63   8.54
19   6.50   8.45
20   6.44   8.44
21   6.40   8.37
22   6.25   8.31
23   6.20   8.23
24   6.16   8.05
25   6.00   8.99

> Map(cbind.fill,less8,bet8and9,great9)
$roll.no
        object     object     object
1   15071A05D2 15071A05G1 15071A05G6
2   15071A05H4 15071A05F7 15071A05D9
3   15071A05H6 15071A05F5 15071A05E0
4   15071A05F1 15071A05D1 15071A05D5
5   16075A0525 15071A05E1 15071A05C1
6   16075A0530 15071A05G8 15071A05F3
7   16075A0529 15071A05H7 15071A05G5
8   15071A05H9 15071A05G9 15071A05D6
9   15071A05E7 16075A0533 15071A05C2
10  16075A0536 15071A05E5 15071A05E6
11 14071A05C1` 15071A05G2 15071A05E8
12  15071A05H3 15071A05I0 15071A05C4
13  15071A05C7 15071A05D8 15071A05E4
14  15071A05H8 15071A05F0 15071A05H1
15  16075A0526 15071A05F4 15071A05G7
16  16075A0528 15071A05H0 15071A05D0
17  16075A0535 15071A05H5 15071A05D7
18  16075A0532 15071A05C9 15071A05H2
19  16075A0531 15071A05F6 15071A05F2
20  15071A05C5 15071A05E3 15071A05G6
21  15071A05C3 15071A05G0 15071A05D9
22  15071A05D3 15071A05C6 15071A05E0
23  15071A05C8 15071A05G3 15071A05D5
24  15071A05F9 15071A05F8 15071A05C1
25  15071A05D4 15071A05G1 15071A05F3

$grade
   object object object
1    7.90   8.99   9.56
2    7.79   8.98   9.53
3    7.77   8.97   9.47
4    7.51   8.91   9.43
5    7.50   8.89   9.40
6    7.50   8.88   9.40
7    7.40   8.85   9.37
8    7.37   8.84   9.34
9    7.33   8.84   9.31
10   7.30   8.83   9.31
11   7.24   8.82   9.31
12   7.23   8.82   9.29
13   7.00   8.81   9.27
14   6.90   8.81   9.25
15   6.80   8.81   9.22
16   6.71   8.76   9.18
17   6.71   8.70   9.11
18   6.63   8.54   9.11
19   6.50   8.45   9.04
20   6.44   8.44   9.56
21   6.40   8.37   9.53
22   6.25   8.31   9.47
23   6.20   8.23   9.43
24   6.16   8.05   9.40
25   6.00   8.99   9.40

> chroll<-as.character(chhh$roll.no)
> chroll
 [1] "15071A05G6"  "15071A05D9"  "15071A05E0"  "15071A05D5"  "15071A05C1"  "15071A05F3"  "15071A05G5" 
 [8] "15071A05D6"  "15071A05C2"  "15071A05E6"  "15071A05E8"  "15071A05C4"  "15071A05E4"  "15071A05H1" 
[15] "15071A05G7"  "15071A05D0"  "15071A05D7"  "15071A05H2"  "15071A05F2"  "15071A05G1"  "15071A05F7" 
[22] "15071A05F5"  "15071A05D1"  "15071A05E1"  "15071A05G8"  "15071A05H7"  "15071A05G9"  "16075A0533" 
[29] "15071A05E5"  "15071A05G2"  "15071A05I0"  "15071A05D8"  "15071A05F0"  "15071A05F4"  "15071A05H0" 
[36] "15071A05H5"  "15071A05C9"  "15071A05F6"  "15071A05E3"  "15071A05G0"  "15071A05C6"  "15071A05G3" 
[43] "15071A05F8"  "15071A05D2"  "15071A05H4"  "15071A05H6"  "15071A05F1"  "16075A0525"  "16075A0530" 
[50] "16075A0529"  "15071A05H9"  "15071A05E7"  "16075A0536"  "14071A05C1`" "15071A05H3"  "15071A05C7" 
[57] "15071A05H8"  "16075A0526"  "16075A0528"  "16075A0535"  "16075A0532"  "16075A0531"  "15071A05C5" 
[64] "15071A05C3"  "15071A05D3"  "15071A05C8"  "15071A05F9"  "15071A05D4" 
> chhh
# A tibble: 68 x 2
   roll.no    grade
   <chr>      <dbl>
 1 15071A05G6  9.56
 2 15071A05D9  9.53
 3 15071A05E0  9.47
 4 15071A05D5  9.43
 5 15071A05C1  9.40
 6 15071A05F3  9.40
 7 15071A05G5  9.37
 8 15071A05D6  9.34
 9 15071A05C2  9.31
10 15071A05E6  9.31
# ... with 58 more rows
> matchroll<-matrix(chroll,nrow=17,ncol=4)
> matchroll
      [,1]         [,2]         [,3]         [,4]         
 [1,] "15071A05G6" "15071A05H2" "15071A05H0" "15071A05E7" 
 [2,] "15071A05D9" "15071A05F2" "15071A05H5" "16075A0536" 
 [3,] "15071A05E0" "15071A05G1" "15071A05C9" "14071A05C1`"
 [4,] "15071A05D5" "15071A05F7" "15071A05F6" "15071A05H3" 
 [5,] "15071A05C1" "15071A05F5" "15071A05E3" "15071A05C7" 
 [6,] "15071A05F3" "15071A05D1" "15071A05G0" "15071A05H8" 
 [7,] "15071A05G5" "15071A05E1" "15071A05C6" "16075A0526" 
 [8,] "15071A05D6" "15071A05G8" "15071A05G3" "16075A0528" 
 [9,] "15071A05C2" "15071A05H7" "15071A05F8" "16075A0535" 
[10,] "15071A05E6" "15071A05G9" "15071A05D2" "16075A0532" 
[11,] "15071A05E8" "16075A0533" "15071A05H4" "16075A0531" 
[12,] "15071A05C4" "15071A05E5" "15071A05H6" "15071A05C5" 
[13,] "15071A05E4" "15071A05G2" "15071A05F1" "15071A05C3" 
[14,] "15071A05H1" "15071A05I0" "16075A0525" "15071A05D3" 
[15,] "15071A05G7" "15071A05D8" "16075A0530" "15071A05C8" 
[16,] "15071A05D0" "15071A05F0" "16075A0529" "15071A05F9" 
[17,] "15071A05D7" "15071A05F4" "15071A05H9" "15071A05D4" 
> less8[sample(nrow(less8)),]
# A tibble: 25 x 2
   roll.no     grade
   <chr>       <dbl>
 1 15071A05C8   6.20
 2 15071A05H3   7.23
 3 16075A0535   6.71
 4 14071A05C1`  7.24
 5 15071A05C3   6.40
 6 15071A05H4   7.79
 7 15071A05H6   7.77
 8 16075A0526   6.80
 9 16075A0536   7.30
10 16075A0529   7.40
# ... with 15 more rows
> less8[sample(nrow(less8)),]
# A tibble: 25 x 2
   roll.no     grade
   <chr>       <dbl>
 1 15071A05C7   7.00
 2 16075A0530   7.50
 3 15071A05C5   6.44
 4 15071A05H3   7.23
 5 15071A05D2   7.90
 6 15071A05F9   6.16
 7 16075A0529   7.40
 8 14071A05C1`  7.24
 9 16075A0525   7.50
10 15071A05C3   6.40
# ... with 15 more rows
> less8[sample(nrow(less8)),]
# A tibble: 25 x 2
   roll.no    grade
   <chr>      <dbl>
 1 15071A05C7  7.00
 2 15071A05H8  6.90
 3 15071A05D2  7.90
 4 15071A05F1  7.51
 5 16075A0531  6.50
 6 15071A05H4  7.79
 7 16075A0525  7.50
 8 16075A0532  6.63
 9 16075A0536  7.30
10 15071A05D3  6.25
# ... with 15 more rows
> less8[sample(nrow(less8)),]
# A tibble: 25 x 2
   roll.no    grade
   <chr>      <dbl>
 1 16075A0531  6.50
 2 16075A0526  6.80
 3 15071A05H9  7.37
 4 15071A05E7  7.33
 5 16075A0525  7.50
 6 16075A0532  6.63
 7 15071A05H3  7.23
 8 15071A05H8  6.90
 9 16075A0536  7.30
10 15071A05C3  6.40
# ... with 15 more rows
> rbind(great9[sample(nrow(great9)),],bet8.5and9[sample(nrow(bet8.5and9)),],bet8.5and8[sample(nrow(bet8.5and8)),],less8[sample(nrow(less8)),])
# A tibble: 68 x 2
   roll.no    grade
   <chr>      <dbl>
 1 15071A05E6  9.31
 2 15071A05F2  9.04
 3 15071A05G7  9.22
 4 15071A05C4  9.29
 5 15071A05C2  9.31
 6 15071A05D9  9.53
 7 15071A05H1  9.25
 8 15071A05D7  9.11
 9 15071A05E4  9.27
10 15071A05E0  9.47
# ... with 58 more rows
> finalchhh<-rbind(great9[sample(nrow(great9)),],bet8.5and9[sample(nrow(bet8.5and9)),],bet8.5and8[sample(nrow(bet8.5and8)),],less8[sample(nrow(less8)),])
> finalchhh
# A tibble: 68 x 2
   roll.no    grade
   <chr>      <dbl>
 1 15071A05D5  9.43
 2 15071A05G5  9.37
 3 15071A05F2  9.04
 4 15071A05H2  9.11
 5 15071A05E6  9.31
 6 15071A05G7  9.22
 7 15071A05E8  9.31
 8 15071A05C1  9.40
 9 15071A05E4  9.27
10 15071A05G6  9.56
# ... with 58 more rows
> matchroll<-matrix(as.character(finalchhh$roll.no),nrow=17,ncol=4)
> matchroll
      [,1]         [,2]         [,3]         [,4]         
 [1,] "15071A05D5" "15071A05D0" "15071A05F4" "16075A0531" 
 [2,] "15071A05G5" "15071A05D9" "15071A05H5" "16075A0536" 
 [3,] "15071A05F2" "15071A05F7" "15071A05F5" "16075A0532" 
 [4,] "15071A05H2" "15071A05D1" "15071A05C6" "15071A05H8" 
 [5,] "15071A05E6" "15071A05H0" "15071A05G3" "15071A05D3" 
 [6,] "15071A05G7" "15071A05G2" "15071A05F6" "15071A05H4" 
 [7,] "15071A05E8" "15071A05H7" "15071A05G0" "16075A0530" 
 [8,] "15071A05C1" "15071A05E1" "15071A05E3" "15071A05D4" 
 [9,] "15071A05E4" "15071A05G8" "15071A05F8" "15071A05E7" 
[10,] "15071A05G6" "16075A0533" "16075A0528" "15071A05F9" 
[11,] "15071A05F3" "15071A05F0" "15071A05F1" "15071A05C3" 
[12,] "15071A05D7" "15071A05D8" "16075A0525" "15071A05H3" 
[13,] "15071A05E0" "15071A05G1" "16075A0535" "15071A05H9" 
[14,] "15071A05C2" "15071A05C9" "15071A05C7" "15071A05C8" 
[15,] "15071A05H1" "15071A05E5" "16075A0529" "14071A05C1`"
[16,] "15071A05D6" "15071A05I0" "16075A0526" "15071A05D2" 
[17,] "15071A05C4" "15071A05G9" "15071A05C5" "15071A05H6"
