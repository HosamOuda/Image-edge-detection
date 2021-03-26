# Image Processing Project 📷🤔

## Description:

A computer vision project that implements different edge detection filters such as such as
<ul>
  <li>Sobel filter </li>
  <li>Perwitt filter</li>
  <li>First-order derivative</li>
  <li>Second-order derivative</li>
</ul>  

then by passing the image through any of these filters so that we can reach our goal 🎉🎉🎊.

## Project porcedure :

<ol>
  <li>We open the current directory where we saved our test image at by using OS library. </li>
  
  <li>By using the CV2 library we read the image path and now we have the image ready to be passed through our filters.</li><br> 
  <img src="https://cdn.discordapp.com/attachments/598537237738815488/824901494205579274/1.PNG" width="370" /> <br>
  
  <li>We apply gaussian mask to the original image to smooth it and blur it by copmputing the gaussain mask array through some mathematical operations and then convolute it with the original image. </li><br>
  <img src="https://cdn.discordapp.com/attachments/598537237738815488/824904776176631868/unknown.png" width="370" /> <br>
  <h3> 🎇🎇 Now we can pass the image through different filters 🎇🎇</h3><br>
  <h3> 🎇🎇 By using Sobel filter 🎇🎇</h3><br>
  <ol>
  <li>We start by using pre-detrmined matrices that intializes the values of the x-direction and y-direction of the filter window</li>
  <li> Pass these 2 matrices along with the blurred image to edge detection function that detect image by comparing the pixel with its neighbors if it has huge junp in it relative to its neighbors 
  then it's an edge and we trace this edge until we reach the end of it </li>
  <li> The edge detector function returns the direction of the edges </li><br>
  <img src="https://cdn.discordapp.com/attachments/598537237738815488/824901522180931624/3_edge_image.PNG" width="370" /> <br>
  <li> By using the directions of edges from the edge detector function we apply the non-maxima algorithm for thinning the edges </li><br>
  <img src="https://cdn.discordapp.com/attachments/598537237738815488/824901534563041310/4_non_maxima.PNG" width="370" /> <br>
  <li> Then we apply double threshold by giving priority to the strong edges and give them the max pixel value and that will priotrize them over the weak irrelevant edges</li><br>
  <img src="https://cdn.discordapp.com/attachments/598537237738815488/824901545413967913/5_double_threshold.PNG" width="370" /> <br>
  <li> Finally we link the weak edges to the strong ones by checking the neighbors of them and set their value to be as high as possible if the have strong edge as their neigbors or 
  otherwise set them to the smallest possible value because in this case they are irrelevant and we don't need to show it</li><br>
  <img src="https://cdn.discordapp.com/attachments/598537237738815488/824901557925576744/6_final_image.PNG"width="370" /> <br>
   <h3 style="text-align:center;">           🎆🎆🎊🎊🎈🎈 We reached our goal using Sobel Filter 🎈🎈🎊🎊🎆🎆 </h3><br>
  </ol>
  
   <h3> 🎇🎇 By using Perwit filter 🎇🎇</h3><br>
   <p> We apply the very same procedure as the sobel but we change in the values of pre-detrmined matrices that intializes the values of the x-direction and y-direction of the   filter window we get a final image like that: </p>
  <img src="https://cdn.discordapp.com/attachments/598537237738815488/824919776911949824/unknown.png"width="370" /> <br>
    <h3> 🎇🎇 By using First-order derivative filter 🎇🎇</h3><br>
   <p> We apply the very same procedure as the sobel but we change in the values of pre-detrmined matrices that intializes the values of the x-direction and y-direction of the   filter window to be centered around x-axis and the y-axis so our final image will be like this: </p>
   <img src="https://cdn.discordapp.com/attachments/598537237738815488/824920497853956096/unknown.png"width="370" /> <br>
        <h3> 🎇🎇 By using Second-order derivative filter 🎇🎇</h3><br>
   <p> As in sobel and perwit and first-order derivative but with differences in the x-direction matrix and y-direction matrix,  our final image for the Second-order derviative filter will be like this: </p>
  <img src="https://cdn.discordapp.com/attachments/598537237738815488/824920932187373588/unknown.png"width="370" /> <br>
</ol>  
