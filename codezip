#include <iostream>
#include <vector>

using namespace std;

// Function to print the chessboard
void printBoard(const vector<int>& board) {
    int N = board.size();
    for (int i = 0; i < N; i++) {
        for (int j = 0; j < N; j++) {
            if (board[i] == j)
                cout << "Q ";
            else
                cout << ". ";
        }
        cout << endl;
    }
    cout << endl;
}

// Function to check if a queen can be placed at (row, col)
bool isSafe(const vector<int>& board, int row, int col) {
    int N = board.size();
    // Check if there's a queen in the same column
    for (int i = 0; i < row; i++) {
        if (board[i] == col)
            return false;
        // Check for diagonal conflicts
        if (abs(row - i) == abs(col - board[i]))
            return false;
    }
    return true;
}

// Recursive function to solve N-Queens problem using backtracking
void solveNQueens(vector<int>& board, int row) {
    int N = board.size();
    if (row == N) {
        // print the solution
        printBoard(board);
        return;
    }
    // Try placing queen in each column of current row
    for (int col = 0; col < N; col++) {
        if (isSafe(board, row, col)) {
            board[row] = col;
            solveNQueens(board, row + 1);
            // Backtrack if no solution found
            board[row] = -1;
        }
    }
}

//solve N-Queens problem
void solveNQueens(int N) {
    vector<int> board(N, -1); // Initialize board with no queens
    solveNQueens(board, 0); // Start from row 0
}
int main() {
    int N;
    cout <<"Enter the number of Queen (N):";
    cin >> N;
    solveNQueens(N);
    return 0 ;
    }


    // This function takes a vector board representing the positions of queens on the
    //chessboard. It prints the board, where 'Q' represents a queen and '.' represents
    //an empty cell.this function is used for placing the position of queen Q represent
    // the position of queen and . represent the position of an empty cell
    // isSafe is used for checking row and col on chess board no other then one queen comes in same row as well as column
