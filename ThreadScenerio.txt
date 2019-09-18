package ThreadScenerio;
public class ThreadClass extends Thread{
    String TName;
    String action;
    
    public ThreadClass(String TName, String action){
        this.TName = TName;
        this.action = action;
    }
    
    @Override
    public void run(){
        for(int i = 1; i <= 10; i++)
            System.out.println(TName + " is " + action);
    }
    
    public static void main(String[] args){
        ThreadClass doyinThread = new ThreadClass("Doyin","Laughing");
        ThreadClass dayoThread = new ThreadClass("Dayo","Washing");
        ThreadClass segunThread = new ThreadClass("Segun","Dancing");
        ThreadClass bolaThread = new ThreadClass("Dayo","Cooking");
        ThreadClass simeonThread = new ThreadClass("Simeon","Eating");
        
        System.out.println("Adeyemi Adedoyin Simeon (209188)\n");
        doyinThread.start(); dayoThread.start(); segunThread.start();
        bolaThread.start(); simeonThread.start();   
    }
    
}
