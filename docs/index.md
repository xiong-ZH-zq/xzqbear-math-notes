---
comments: true
---
# 这里是 xzqbear 的数学笔记博客存放站
本站由 `mkdocs` 生成，现在仍然在更新当中.
## 关于我
![cover](imgs/profile.jpg){ align=left width="200" }
我是来自NKU的一名**数学系**大类学生，喜欢数学与技术，以下是联系我的一些方式：

- :material-mail: NKU邮箱(Email) ： `xzqbear@mail.nankai.edu.cn`
- :simple-github: Github 个人主页：[xiong-ZH-zq (xzqbear) (github.com)](https://github.com/xiong-ZH-zq)
  
这里的笔记内容主要是NKU数学类课程的课程笔记，参考的教材也不仅仅只局限于NKU使用的教材。

如果喜欢这个笔记存放站，欢迎给一个 Star :material-star: 或者 Fork :fontawesome-solid-code-fork: 这个仓库。

本站公式采用 $\mathrm{\LaTeX}$ 公式（具体一些是 KaTeX），同时绘图使用 TikZJax 或 Python 等工具导出.

<script type="text/tikz">
\begin{tikzpicture}
\definecolor{color0}{rgb}{0.886274509803922,0.290196078431373,0.2}
\definecolor{color1}{rgb}{0.203921568627451,0.541176470588235,0.741176470588235}
\begin{axis}[
axis background/.style={fill=white!89.8039215686275!black},
axis line style={white},
tick align=outside,
tick pos=left,
title={Simple plot \(\displaystyle \frac{\alpha}{2}\)},
x grid style={white},
xlabel={time (s)},
xmajorgrids,
xmin=-0.095, xmax=1.995,
xtick style={color=white!33.3333333333333!black},
y grid style={white},
ylabel={Voltage (mV)},
ymajorgrids,
ymin=-1.1, ymax=1.1,
ytick style={color=white!33.3333333333333!black}
]
\addplot [line width=1.64pt, color0, mark=*, mark size=3, mark options={solid}]
table {%
0 0
0.1 0.587785252292473
% [...]
1.9 -0.587785252292473
};
\addplot [line width=1.64pt, color1, mark=*, mark size=3, mark options={solid}]
table {%
0 1
0.1 0.809016994374947
% [...]
1.9 0.809016994374947
};
\end{axis}

\end{tikzpicture}
</script>
例如上图的函数图像就是一个 TikZ 图像. 
