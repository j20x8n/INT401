java c
INT401: Fundamentals of Machine Learning
Fall Semester
Lab 6: Naive Bayes Classifier
6.1          Objectives
•    Understand   the   knowledge   on   Naive   Bayes   classifier.
•    Learn   how   to   create   a   Naive   Bayes   classifier   to   solve   a   toy   problem   on   prediction.
6.2          Dataset   DescriptionThis   is   atoy   dataset, which   contains   21   attribute   feature   columns   and   one   class   label   column.    The   dataset   is a   two-class   classification   problem, where   the   first   column   is   the   class   label.    All   attributes   have   been   mapped from   text   descriptions   to   numbers, where   the   same   numbers   in   the   same   column   represent   the   same   attribute values.   The dataset is divided into   a   training   set   toy   train.csv   and   a   test   set   toy   test.csv,   where   the   training   set   and   the   test   set   contain   7600   samples   and   524   samples   respectively.
6.3          Naive   Bayes   Classifier
6.3.1          Load   dataset
•    (10   marks)      Read   the   training   dataset   into   a   dataframe.
•    (10   marks)      Read   the   test   dataset,   which   will   be   used   to   estimate   the   classification   accuracy.
6.3.2          Maximum   Likelihood   Estimation
When   X   contains   M   attributes   which   satisfy   the   conditional   independence   assumption,   we   have

where   Xi    is   the   i-th   attribute   and   Y   is   the   class   label.    Our   goal   is   to   train   a   classifier   that   will   output   the   probability   distribution   over   possible   values   of Y   ,   which   will   take   on   its   possible   value   k   =   1,   2,   ···,K   is

Note   that   for   any   example   X,   the   probability   P(X)   =   P(X1   ,   X2, ···,   XM   )   is   constant.    We   can   estimate   these   parameters   using   maximum   likelihood   estimates.
•    (20   marks)      Estimate the   prior   probability
•    (30   marks)    Estimate   the   conditional   probability
It is noted that the #D{x} operator denotes   the   number   of elements   in   the   set   D   that   satisfy   property   x   and   Nj    means that   attribute   Xj      has   Nj      different   values.
6.3.3          Model   Inference
•    (20   marks)      For   K   c代 写INT401: Fundamentals of Machine Learning Fall Semester Lab 6: Naive Bayes ClassifierPython
代做程序编程语言ategories,   we   calculate   the   posterior   probability   of each   category   separately   for   X   =   [x1   ,   x2,   ···,   xM   ]T    and get      
Note:    If   the   conditional   probability   P(ˆ)(Xj      =   xj |Y   =   yk   )   that   does   not   appear   in   the   training   set   is   needed   in   the   test   set,   then   the   conditional   probability   under   class   k   should   be           •    (10   marks)       For   each   X,   we   assign   X   to   the   class   with   the   largest   posterior   probability   logP(ˆ)(Y   = yk   |X).
6.4          Lab   Report
•   Write   a   short   report   which   should   contain   a   concise   explanation   of your   implementation,   results   and   observations.
For   the   score   of each   step,   such   as   15   points,   the   proportion   of the   three   parts   to   the   total   score   is   as   follows:
–      Explanation   of   the   execution   of   this   step   (   50% ):   how   to   design   the   data   structure, how   to   design the   algorithm   to   realize   this   step;   how   do   you   think   about   this   problem
–    Code   and   comments   (   30%   ):   Whether   the   code   is   correct,   attach   comments   to   help   understand the   code
–      Results   and   interpretation   (   20%   ):   Whether   the   running   results   are   correct,   explain   the   results   to   a   certain   extent,   or   what   you   find   from   them.      Please   insert   the   clipped   running   image   into your   report   for   each   step.
•    Submit   the   report   and   the   python   source   code   with   the   suitable   comments   electronically   into   the   learning   mall.
•   It   is   highly   recommended   to   use   the   latex   typesetting   language   to   write   reports.
•      The report in pdf format and python source code of your implementation should be   zipped   into   a   single   file.   The   naming   of   report   is   as   follows:
e.g.   StudentID   LastName   FirstName   LabNumber.zip   (123456789   Einstein   Albert         1.zip)
6.5          Hints
Please   refer   to   the   lecture   slides.
•      Latex   IDE: texstudio
•      Python   IDE:   pycharm   or   vscode
•      Use   the   python   numpy   and   scipy   library   flexibly.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
