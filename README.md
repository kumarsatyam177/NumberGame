import java.util.scanner;
public class NumberGame
{
    public static void main(string[]args)
    {
        scanner sc=new scanner(system.in);
        int chances=8;
        int finals=0;
        boolean playAgain=true;
        systam.out.printin("Welcome Buddy!");
        system.out.printin("hey buddy you have about"+chances+"to win the game");
        while(playAgain)
        {
            int raud =getrandN(1,100);
            boolean guess = false;
            for(int i=0;i<chances;i++)
            {
                system.out.printin("chance"+(i+1)+"Enter your guess:");
                int user=sc.nextInt();
                if(user==sc.rand)
                {
                    guess=true;
                    finals+=1;
                    system.out.printin("you won it."
                    );
                    break;
                }
                else if(user>rand){
                    system.out.printin("too high");
                }
                else{
                    system.out.printin("too low");
                }
            }
                if(guess==false){
                    system.out.printin("sworry buddy.you lost the chances.the number is "+rand);
                    
                }
                system.out.printin("Do you want to play again(y/n");
                string pA=sc.next();
                playAgain=pA.equalsIgnoreCase("y");
            }
            system.out.printerin("that's it buddy,hope you enjoying it");
            system.out.printerin("here is your score"+finals);
    }
            public static int getrandN(int min, int max)
            {
                return(int)(Math.rendom()*(max-min+1)+min);
            
            
        }
}
}
