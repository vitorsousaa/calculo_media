# calculo_media
calculo media 

package media;
import java.util.Scanner;
 
public class CalcularMedia {
 
    public static void main(String[] args){
 
    //Criação do objeto Scanner	.
    Scanner notas = new Scanner(System.in);
    
    /*Declaração das variáveis:
    1º nota, 2º nota, 3º nota, 4º nota, Média e Nota do Exame Final, respectivamente. */ 
    double n1, n2, n3, n4, n5, n6, n7 , n8,  media, nExame;
    
    //Recebe primeira nota.
    System.out.println("Digite a nota 1:\n");
    n1 = notas.nextDouble();
    
    //Recebe segunda nota.
    System.out.println("Digite a nota 2:\n");
    n2 = notas.nextDouble();
    
    //Recebe terceira nota.
    System.out.println("Digite a nota 3:\n");
    n3 = notas.nextDouble();
    
    //Recebe quarta nota.
    System.out.println("Digite a nota 4:\n");
    n4 = notas.nextDouble();
    
    //Recebe quinta nota.
    System.out.println("Digite a nota 5:\n");
    n5 = notas.nextDouble();
    
    //Recebe sexta nota.
    System.out.println("Digite a nota 6:\n");
    n6 = notas.nextDouble();
    
    //Recebe setima nota.
    System.out.println("Digite a nota 7:\n");
    n7 = notas.nextDouble();
    
    //Recebe oitava nota.
    System.out.println("Digite a nota 8:\n");
    n8 = notas.nextDouble();
    
    //Calcula a média com os determinados pesos.
    media = (n1*1,25 + n2*1,25 + n3*1,25 + n4*1,25 + n5*1,25 + n6*1,25 + n7*1,25 + n8*1,25)/10;
    
    //Caso de aluno aprovado por média.
    if(media >= 7.0){
    	
    	//Imprime a média e imprime que o aluno foi aprovado.
        System.out.printf("Media: %.1f\nAluno aprovado por media.\n", media);}
        
    //Caso de aluno em Exame final
    else if(media >= 5.0 && media < 7.0){
    	
    	//Imprime a média e imprime que o aluno está no exame final.
        System.out.printf("Media: %.1f\nAluno em exame.\n", media);
        
        //Recebe a nota do exame final.
        System.out.println("Digite a nota do exame:\n");
        nExame = notas.nextDouble();
        
        //Imprime a nota do exame final.
        System.out.printf("Nota do exame: %.1f\n", nExame);
        
        //Recalcula a média para média após o exame final.
        media = (media + nExame)/2;
        
        //Caso de aluno aprovado.
        if(media >= 5){
           System.out.printf("Aluno aprovado.\nMedia final: %.1f", media);}
        
        //Caso de aluno reprovado.
        else{
           System.out.printf("Aluno reprovado.\nMedia final: %.1f", media);}}
    
    //Caso de aluno reprovado por média.
    else{
        System.out.printf("Media: %.1f\nAluno reprovado por media.\n", media);}
        
    }
 
}
