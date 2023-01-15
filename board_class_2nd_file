package Tic_Tac_Toe_game;

public class board_class {
   private char board[][];
   private static final int boardSize = 3;
   private char p1Symbol , p2Symbol;
   private int count;//to count numbers of cells that are filled
   
   private static final char empty = ' ';
   public static final int PLAYER1WINS = 1;
   public static final int PLAYER2WINS = 2;
   public static final int DRAW = 3;
   public static final int INCOMPLETE = 4;
   public static final int INVALIDMOVE = 5;

   
   public board_class(char p1Symbol , char p2Symbol) {
	   
	   board = new char[boardSize][boardSize];
	   for(int i = 0 ; i < boardSize ; i++) {
		   for(int j = 0 ; j < boardSize ; j++) {
			   board[i][j]=  empty;
		   }
	   }
	   this.p1Symbol = p1Symbol;
	   this.p2Symbol = p2Symbol;
   }
   public void print() {
	   System.out.println("_______________");
	   for(int i = 0 ; i<boardSize ; i++) {
		   for(int j = 0 ; j < boardSize ; j++) {
			   System.out.print("|"+board[i][j]+"|");
		   }
		   System.out.println();
	   }
	   System.out.println("_______________");
   }
   
   public int move(char symbol , int x , int y) {
	   
	   if(x<0 || x>= boardSize || y<0 || y>= boardSize || board[x][y] != empty)
	          return INVALIDMOVE;
	   
	   board[x][y] = symbol;
	   count++;
	   
	   if( board[x][0] == board[x][1] && board[x][0] == board[x][2]) { 
		return symbol == p1Symbol ? PLAYER1WINS : PLAYER2WINS;
	   }else if(board[0][y]==board[1][y] &&  board[0][y]==board[2][y] ) {
		   return symbol == p1Symbol ? PLAYER1WINS : PLAYER2WINS ;
	   }else if( board[0][0]!=empty && board[0][0] == board[1][1] && board[1][1] == board[2][2]) {
		   return symbol == p1Symbol ? PLAYER1WINS : PLAYER2WINS ;
	   }else if( board[0][2]!=empty && board[0][2] == board[1][1] && board[1][1] == board[2][0]) {
		   return symbol == p1Symbol ? PLAYER1WINS : PLAYER2WINS ;
	   }else if(count == boardSize*boardSize) {
		   return DRAW;
	   }else {
	   return INCOMPLETE;
	   }
   }
   
}
