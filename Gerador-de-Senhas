import secrets
import string

def imprimir_senha (s):
    print('A senha gerada foi: ', end="")
    print( s)


def gerar_novamente ():
    while True:
        res = str(input('Deseja gerar outra senha? [S/N]: ')).upper().strip()
        if res in ('S', 'N'):
            return res
        else:
            print('S para sim e N para não.')


def gerar_senha(t, d):
    return '' .join(secrets.choice(d) for _ in range(t))


print('F para [Fácil] (8 dígitos apenas números)\n'
      'M para [Médio] (10 dígitos números e letras)\n'
      'D para [Difícil] (15 dígitos números letras e símbolos)')

nivel = str(input('Qual nivel de segurança você deseja? ')).upper().strip()
escolha = 'S'.upper().strip()

while escolha == 'S':
    if nivel == 'F':
        tamanho = 8
        digitos = string.digits


    elif nivel == 'M':
        tamanho = 10
        digitos = string.ascii_letters + string.digits


    else:
        tamanho = 15
        digitos = string.ascii_letters + string.digits + string.punctuation

    senha = gerar_senha(tamanho, digitos)
    imprimir_senha(senha)
    escolha = gerar_novamente()
