# uas1.java


 int stack[]=new int[3];
   
    public void push(int value){
        if(stack[0]==0){
            stack[0]=value;
        }else if(stack[1]==0){
            stack[1]=value;
        }else if(stack[2]==0){
            stack[2]=value;
        }else{
            isFull();
        }
       
    }
    public void isFull(){
        System.out.println("STACK IS FULL");
    }
    public void pop(){
       if(stack[2]!=0){
            stack[2]=0;
        }else if(stack[1]!=0){
            stack[1]=0;
        }else if(stack[0]!=0){
            stack[0]=0;
        }
        else{
            isEmpty();
        }
    }
    public void isEmpty(){
        System.out.println("STACK IS EMPTY");
    }
    public void clear(){
        stack[0]=0;
        stack[1]=0;
        stack[2]=0;
    }
    public void cetak(){
        for(int i=0;i<stack.length;i++){
            if(stack[i]!=0){
            System.out.println(stack[i]+" ");
            }
        }
    }
    public static void main(String[] args) {
        Stack1 s=new Stack1();
        s.push(5);
        s.push(3);
        s.push(2);
        s.push(4);
        System.out.println("--------PUSH--------");
        s.cetak();
        s.pop();
        System.out.println("--------POP--------");
        s.cetak();
    }

