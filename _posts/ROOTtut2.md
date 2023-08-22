---
layout: post
mathjax: true
categories: media
title: "CERN ROOT Beginner Notes 2"
---

Source: [CERN ROOT Tutorials by Physics Matter](https://www.youtube.com/watch?v=KPz-dNjdx40&list=PLLybgCU6QCGWLdDO4ZDaB0kLrO3m). This note is for personal learning purposes and has no commercial use.

#### 10 - Plotting Data with Error Bars
Suppose we have a txt file named `data3.txt`:
```C
// x value, y value, error in x direction, error in y direction
1 1 0 0.1
2 2 0 0.2
3 3 0 0.3
4 4 0 0.4
5 5 0 0.5
```
To plot the error bars:
```C
void tut10()
{
    TCanvas *c1 = new TCanvas();
    TGraphErrors *gr = new TGraphErrors();

    fstream file;
    file.open("data3.txt",ios::in);

    double x,y,ex,ey;
    int n = 0;
    while(1)
    {
      file >> x >> y >> ex >> ey;
      n = gr->GetN();
      gr->SetPoint(n,x,y);
      gr->SetPointError(n,ex,ey);

      if (file.eof()) break;
    }
    gr->Draw("A*");
}

```
