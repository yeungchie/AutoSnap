# AutoSnap  

用于垂直线段的自动吸附  

* Author:YEUNGCHIE  

* Tips:需要设置一下工艺相关的信息。在第50行和300行左右。只对path/pathseg有效，且都会变成pathseg。  

* Describe:  

> AutoSnap(l_pathsobj)  
  l_pathsobj:包含两条path/pathseg对象的list。
  用于快速吸附两条相互垂直的path/pathseg。

> AutoSnapByHi(  
  ?cv d_cv  
  ?mode t_mode  
  ?snapbynet g_switch  
  ?rmmpp g_switch  
  ?addvia g_switch  
  ?viamin l_minsize  
  )  
  ?cv:默认当前编辑的cellview。  
  ?mode:设置操作方式，可选"click"吸附鼠标最接近的两条path和"line"批量吸附两组垂直path，默认是"click"。  
  ?snapbynet:用于XL下根据net来匹配吸附，默认nil。此项关闭时，上面"line"方式会根据画线的方向来选择吸附后交叉与否。  
  ?rmmpp:是否不对MPP操作，默认nil。此项开启时，会将MPP的金属层复制并延伸来做吸附操作。  
  ?addvia:是否打孔，默认nil。因为打孔的情况太多很多时候需要手动调整，开启时会在交叉点打1x1的孔。  
  ?viamin:打孔的最小规格，输入为list。例如list(2 1)表示横向两个孔，纵向一个孔。  

> AutoSnapByClicks()  
  AutoSnapByHi(?mode "click")的连击模式。  
