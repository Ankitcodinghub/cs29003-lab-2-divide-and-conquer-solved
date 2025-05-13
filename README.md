# cs29003-lab-2-divide-and-conquer-solved
**TO GET THIS SOLUTION VISIT:** [CS29003 Lab 2-Divide and Conquer Solved](https://www.ankitcodinghub.com/product/cs29003-lab-2-divide-and-conquer-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92896&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS29003 Lab 2-Divide and Conquer Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column"></div>
</div>
<div class="layoutArea">
<div class="column">
Problem Statement

</div>
</div>
<div class="layoutArea">
<div class="column">
You have joined as a trainee in an Institution researching on creating devices to help people with defective eyesight. You have been assigned to a group which deals with the binary eyesight defect, where a person can only see 2 colors, black and white. This means that when 2 objects have a greater contrast than a particular threshold, then they can be perceived as different.

They are at the initial phases of the project and they want to understand and stress on the difficulties faced by these people in recognizing objects and the loss of depth perception.

Since you are still a trainee you have been tasked to get the perspective of users on a set of rectangular objects kept on a table.

Imagine that you are looking right at it, and you cannot see the top of these objects (this simulates the irrelevance of depth information). The objects are of various colours and the background is white, and it is known that the defective eye will not be able to differentiate between each of the objects but there is enough contrast to differentiate between the objects and the background.

Using the divide and conquer technique, devise an algorithm to convert the input of a normal vision (Figure 1(a)) to that of the defective vision (Figure 1(b)), and implement it in C++/C .

(a) objects appearing to normal vision (b) objects appearing to defective vision Figure 1: Images as seen by the 2 visions

Note: Figure 1(b) does not accurately represent the image perceived by the defective eye. The silhouette would be completely filled in that case.

Input

The number of rectangular boxes N. The geometric information of each rectangular box is represented by a triplet of integers [Li , Ri , Hi ], where Li and Ri are the x coordinates of the left and right edge of the ith box, respectively, and Hi is its height. It is guaranteed that:

0􏰀Li,Ri 􏰀INT MAX 0&lt;Hi 􏰀INT MAX

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Ri − Li &gt; 0

You may assume all boxes are perfect rectangles grounded on an absolutely flat surface at height 0.

Output

The output is a list of “key points” (red dots in Figure 1(b)) in the format of

[[x1, y1], [x2, y2], [x3, y3], …]

A key point is the left endpoint of a horizontal line segment.

Note that the last key point, where the rightmost box ends, is merely used to mark the termination of the outline, and always has zero height. Also, the ground in between any two adjacent boxes should be considered part of the outline contour.

Na ̈ıve Algorithm

This will be an incremental approach, where we will build the outline by merging it with every box in the order which is given. (Remember that the input is not sorted in any order)

Here, the inputs are stored in boxes array described in detail in the Input section above.

<pre>typedef struct {
   int left; // x coordinate of left side
   int ht; // height
   int right; // x coordinate of right side
</pre>
<pre>} Box;
typedef struct { // A Point in Outline
</pre>
<pre>   int x; // x coordinate
</pre>
<pre>   int y; // height or the y coordinate
} Point;
</pre>
<pre>boxes is the input array of Box datatype
outline = [] // list of Point datatype, so that deletion and insertion costs O(1)
for b_i in boxes: // O(N)
</pre>
<pre>    find j in outline with b_i.left &lt; outline_j.x // O(N)
    //need to combine this point with the outline
    if outline_{j-1}.y&gt;=b_i.ht: // if the height of the previous point is higher than this
</pre>
<pre>       no need to make any changes
</pre>
<pre>    else
       if outline_{j-1}.x==b_i.left: // if the prev point has the same position
</pre>
<pre>           outline_{j-1}.y = b_i.ht // we know that this point has higher height
       else
</pre>
<pre>           insert a new point
           j++
</pre>
<pre>    for points in outline from index j to k where b_i.right&lt;outline_k.x // O(N)
       do remove points from the outline where the height falls below that of b_i
</pre>
<pre>    //in the way we added the left point make a similar combination on the right point
        (b_i.right, 0)
</pre>
end

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Time complexity: O(N2)

Can you use Divide and Conquer to devise an algorithm with a complexity of O(Nlog(N))?

Sample Test Cases Test Case 1

5

2 9 10

3 7 15

5 12 12 15 20 10 19 24 8

<pre>  Outline :
  [[2,10],[3,15],[7,12],[12,0],[15,10],[20,8],[24,0]]
</pre>
Test Case 2

7

057

5 10 7

5 10 12 10 15 7 15 20 7 15 20 12 20 25 7

<pre>  Outline :
  [[0,7],[5,12],[10,7],[15,12],[20,7],[25,0]]
</pre>
Test Case 3

2 023 253

<pre>  Outline :
  [[0,3],[5,0]]
</pre>
Test Case 4

3 121 122 123

<pre>  Outline :
  [[1,3],[2,0]]
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Implementation Instructions

We will be providing a header file, which you need to include in your program (C/C++).

All the input and output technicalities have been handled in the process() function of the header file. You are free to define structures and classes of your own but make sure to keep the end points compatible.

You sample submission should be as follows

<pre>// 18CS30004\_G03\_Assign2.c/cpp
</pre>
<pre>#include "assign2.h"
Point* findOutLine(Box boxes[], int size, int&amp; outputsize){
</pre>
<pre>    Point* point_array;
</pre>
<pre>    // here solve the problem, where boxes contain the input data and size is the number of
        boxes on the table
</pre>
<pre>    // set outputsize to the number of points in Point array you are yet to return
</pre>
<pre>    return point_array;
}
</pre>
<pre>int main(){
    process();
</pre>
return 0; }

Note : Do not include any other header files.

File Naming Convention

Please note that your submissions will not be evaluated unless you follow the below specified file naming convention for the program file. &lt;ROLLNO(IN CAPS)&gt; Assign&lt;Assign No&gt; G&lt;Group No&gt;.c/cpp

Eg: 18CS30004 G03 Assign2.c / 18CS30004 G03 Assign2.cpp

</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
