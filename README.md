#include <stdio.h>
#include <stdlib.h>
#include <string.h>

typedef struct users
{
    char usuario[11];
    char senha[11];
    struct Login *proximo;
}Login;

Login *ListaUsers = NULL;


void cadastroUser()
{
    Login *novoUser = (Login*) malloc(sizeof(Login));
    novoUser->proximo = NULL;
    Login *aux = ListaUsers;

    printf("---> Cadastro <---\n");
    printf("\nLogin: ");
    scanf("%10s",novoUser->usuario);
    printf("\Senha: ");
    scanf("%10s",novoUser->senha);
    if(ListaUsers==NULL)
    {
        ListaUsers=novoUser;
    }
    else
    {
        while(aux->proximo!=NULL)
        {
            aux=aux->proximo;
        }
        aux->proximo=novoUser;
    }
}
int main()
{

    

    if(strcmp(senhaPadrao,senhaDigitada) == 0)
    {
        printf("\nAcesso Permitido");
    }else{
        printf("\nAcesso negado");
    }

    printf("\n\n**** Senhas ****\n");
    printf("\n--> %s <--",senhaPadrao);
    printf("\n--> %s <--",senhaDigitada);

    return 0;
}
