# triangulo
programacion visual de un triangulo, su area, perimetro y semiperimetro
package programacion.visual;

import java.util.Scanner;

/**
 *
 * @author Eder
 */
public class ProgramacionVisual {
    private Float a;
    private Float b;
    private Float c;

public ProgramacionVisual(){
    
}    

public Float perimetro(){//primer comportamiento
    return a+b+c;
}  
public Double area(){//segundo comportamiento
    float s=semiperimetro();
    return Math.sqrt(s*(s-a)*(s-b)*(s-c));
}
public Float semiperimetro(){//tercer comportamiento
    return perimetro()/2;
}
public void geta(Float t){//funciones para introducir las medidas
    a=t;
}
public Float seta(){
    return a;
}
public void getb(Float t){//funciones para introducir las medidas
    b=t;
}
public Float setb(){
    return b;
}
public void getc(Float t){//funciones para introducir las medidas
    c=t;
}
public Float setc(){
    return c;
}

  
    public static void main(String[] args) {
        float a,b,c;
        Scanner teclado=new Scanner(System.in);
        System.out.println("Vamos a sacar perimetro, semiperimetro y perimetro de un traingulo\nIntroduce a,b y c");
        a=teclado.nextFloat();
        b=teclado.nextFloat();
        c=teclado.nextFloat();
        ProgramacionVisual t1=new ProgramacionVisual();
        t1.geta(a);
        t1.getb(b);
        t1.getc(c);
        System.out.println("el area es: "+t1.area()+"\nEl perimetro es:"+t1.perimetro()+"\nel semiperimetro es:"+t1.semiperimetro());
    }
    
}

