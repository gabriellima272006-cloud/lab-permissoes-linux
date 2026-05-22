# Laboratório de Controle de Acesso e Permissões no Linux Ubuntu 🛡️💻

Neste laboratório prático, simulei o ambiente real de uma empresa usando uma máquina virtual Ubuntu. O objetivo foi aplicar o **Princípio do Menor Privilégio**, garantindo a **Confidencialidade** da Tríade CIA ao trancar dados sensíveis contra usuários não autorizados.

## 🛠️ Ferramentas Utilizadas
* Sistema Operacional: Linux Ubuntu (VirtualBox)
* Comandos de Terminal: `mkdir`, `chmod`, `adduser`, `su`
## 🚀 Passos de Execução

### Passo 1: Criação da Pasta Segura
Criação do diretório para armazenar os arquivos confidenciais do gerente:
```bash
Passo 2: Bloqueio de Permissões (Defesa)
Configuração das permissões para que apenas o Dono e o Grupo tenham acesso total, bloqueando completamente o resto do mundo (Outros):

Bash
chmod 770 arquivo
Resultado visto com ls -l: drwxrwx--- (o final --- prova que outros usuários não leem, não escrevem e não entram na pasta).

Passo 3: Simulação do Ataque (O Invasor)
Criação de um usuário de testes para simular um hacker tentando invadir o sistema:

Bash
sudo adduser invasor
Ao alternar para o usuário invasor (su - invasor) e tentar forçar a entrada na pasta confidencial:

Bash
cd /home/gabriel-de-lima-santos/arquivo
❌ Resultado do Teste
O sistema operacional agiu exatamente como planejado e barrou o ataque na hora, exibindo a mensagem:
bash: cd: Permissão negada

Defesa validada com sucesso! 🛡️
