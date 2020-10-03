# PacmanSearch
Question 1 (3 points): Finding a Fixed Food Dot using Depth First Search
   Dùng CTDL Stack(mỗi phần tử của stack gồm trạng thái kế tiếp và đường đi đến đó, đẩy các trạng thái tiếp theo vào Stack, 
   pop để lấy phần tử đầu Stack rồi đánh dấu trạng thái đã được duyệt, lặp lại cho đến khi stack rỗng


Question 2 (3 points): Breadth First Search
   Tương tự bài 1, thay stack bằng Queue


Question 3 (3 points): Varying the Cost Function
   Dùng CTDL PrirorityQueue (mỗi phần tử của PQ gồm trạng thái kế tiếp, đường đi đến đó và chi phí), PQ sẽ ưu tiên chi phí nhỏ nhất,
   làm giống bài 1 và bài 2

Question 4 (3 points): A* search
   hàm f được tính bằng tổng chi phí đi đến trạng thái kế tiếp và hàm heuristic, PQ sẽ ưu tiên f nhỏ nhất, làm giống bài 3

Question 5 (3 points): Finding All the Corners
   cài đặt các hàm getStartState, isGoalState, getSuccesors
   getStartState
	trả về tuple lưu vị trí bắt đầu của pacman và các góc đã đc thăm
   isGoalState
        trả về true nếu tất cả các góc đã được thăm, false nếu ngược lại

   getSuccesors
	trả về các trạng thái tiếp theo, bằng cách:
	   kiểm tra nếu vị trí kế tiếp không phải tường thì đi tiếp, nếu là góc thì đánh dấu góc đã thăm

Question 6 (3 points): Corners Problem: Heuristic
    cài đặt hàm cornersHeuristi
	heuristic được đánh giá bằng cách kiểm tra những góc chưa được thăm, nếu chưa được thăm thì heuristic sẽ là max của 
	đường đi ngắn từ vị trí hiện tại của pacman đến các góc (đi theo từng ô và đi theo 4 hướng, giả sử không có vật cản)

Question 7 (4 points): Eating All The Dots
    cài đặt hàm foodHeuristic
	heuristic là max của đường đi từ vị hiện tại của pacman đến các dots
	(đường đi từ vị trí hiên tại của pacman đến 1 dot được tính bằng hàm mazeDistance)

Question 8
    cài đặt hàm isGoalState của class AnyFoodSearchProblem, hàm findPathToClosestDot
    isGoalState
	kiểm tra xem vị trí hiện tại của pacman có trùng với vị trí của thức ăn không
	nếu có true, trả về false nếu ngược lại
    findPathToclosetDot
        dùng hàm ucs đã cài ở bài 3 trả về đường đi đến dot gần nhất
    
    
