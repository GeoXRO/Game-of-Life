public class Solution {
    public void gameOfLife(int[][] board) {
        int m = board.length;
        int n = board[0].length;
        int[][] directions = {
                { -1, -1 }, { -1, 0 }, { -1, 1 },
                { 0, -1 }, { 0, 1 },
                { 1, -1 }, { 1, 0 }, { 1, 1 }
        };

        int[][] copyBoard = new int[m][n];
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                copyBoard[i][j] = board[i][j];
            }
        }

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                int liveNeighbors = 0;
                for (int[] direction : directions) {
                    int r = i + direction[0];
                    int c = j + direction[1];

                    if (r >= 0 && r < m && c >= 0 && c < n && copyBoard[r][c] == 1) {
                        liveNeighbors++;
                    }
                }

                if (copyBoard[i][j] == 1) {
                    if (liveNeighbors < 2 || liveNeighbors > 3) {
                        board[i][j] = 0;
                    }
                } else {
                    if (liveNeighbors == 3) {
                        board[i][j] = 1;
                    }
                }
            }
        }
    }
}
