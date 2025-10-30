### Fazendo o Ubuntu reconhecer os demais sistemas do computador e aparecer para escolher o sistema na inicialização do computador
 Altere as configurações do grub para ele aparecer na inicialização do computador
```
  sudo nano /etc/default/grub
```
  - Localize a linha que contém GRUB_TIMEOUT_STYLE e altere seu valor de hidden para menu:
```
GRUB_TIMEOUT_STYLE=menu
```
- Na linha GRUB_TIMEOUT defina o tempo que o grub vai esperar para o usuário selecionar o sistema
```
GRUB_TIMEOUT=10
```
Nesse caso, foi definido 10, que será o tempo em segundos antes de carregar o sistema selecionado.

- Salve o arquivo com o comando Ctrl + O e Ctrl + x para sair

- Digite o comando abaixo para reconhecer todos os sistemas
```
update-grub
```
- Reinicie o computador
