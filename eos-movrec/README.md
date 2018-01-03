### O que é?
O software eos Movrec é uma alternativa Open Source para o Canon EOS Utility, proprietário e apenas disponível para Apple OSX e Microsoft Windows. 

### O que ele faz? 
O programa tem entre as principais utilidades, gerenciar câmeras Canon através do computador, realizando filmagens em até 24 quadros por segundo, salvas no computador, como também fotografias.   
Algumas funções estão disponiveis, como controle de foco, abertura e ISO.   

### Por que Docker? 
Infelizmente o desenvolvimento do softwares está parado e dependendo de bibliotecas antigas, em alguns casos. Tornando a tarefa de "compilação" confusa para alguns usuários.   
Para a sorte dos usuários da distribuição Ubuntu 14.04, existe a versão binária disponível através de PPA e sendo assim, utilizando-se do poder dos containers, foi criado um dockerfile que permite a utilização quase que universal da ferramenta. 

### Como usar?
Dependências:    
 - docker   
 - espaço em disco para a imagem e para os vídeos   
- Claro, uma Canon :)  

1° - Clone o repositório:
 - git clone [https://github.com/rtomkiel/dockerfiles.git](https://github.com/rtomkiel/dockerfiles.git)   

2° - Entre na pasta correta
 - cd eos-movrec   

3° - Crie a imagem   
 - docker build -t eos-movrec .   

4° - Dê permissão de execução ao script   
 - chmod +x eos  

5° - Execute o script "eos"   
 - sh eos

6° - Divirta-se :D 


#### Observações
 - Não esqueça de conectar a câmera antes de executar o script.   
 - Você pode usar sua câmera para transmissões com softwares como OBS.   
 - Edite o script para alterar a pasta padrão onde o vídeo resultante é salvo. 
 - Você pode copiar o script para a pasta **/usr/bin**, criando um lançador. Sendo mais criativo, até um lançador .desktop em **usr/share/applications**   


### Links:

[Fonte do EOS Movrec](https://sourceforge.net/projects/eos-movrec/)   
[PPA Utilizado](https://launchpad.net/~dhor/+archive/ubuntu/myway)   
[Link com a dica do PPA](http://www.edivaldobrito.com.br/gravar-videos-com-uma-antiga-dslr-canon/)  
