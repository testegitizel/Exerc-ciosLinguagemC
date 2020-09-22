# Exerc-ciosLinguagemC
Aqui estão meus exercícios da faculdade
int main()
{
   struct cad_func {
      char nome[40];
      char tel[15];
      float venda;
  };

struct cad_func funcionario[3];
int i,posmaior;
float maiorvenda;


for (i=0;i<3;i++){
    
  printf("Digite o nome do funcionário:");
  scanf("%s", &funcionario[i].nome);
  printf("Digite o número do telefone:");
  scanf("%s", &funcionario[i].tel);
  printf("Digite o valor da venda:");
  scanf("%f", &funcionario[i].venda);
    
}

for(i=0;i<3;i++){
    
    if(funcionario[i].venda>100) {
        
         printf("\nNome do funcionário com venda maior que R$100,00:%s",funcionario[i].nome);
        break;
    }
    
    if(i=0) {
        maiorvenda=funcionario[i].venda;
        posmaior=i;
    }
    else
     
      if(funcionario[i].venda>maiorvenda) {
          maiorvenda=funcionario[i].venda;
          posmaior=i;
      }

    
}


   printf("\nFUNCIONÁRIO QUE REALIZOU MAIOR VENDA!");
   printf("\n%s",funcionario[posmaior].nome);
   printf("\n%s", funcionario[posmaior].tel);
