# Relatorio de Formatacao
## Aula 06 dia 26/10/2023
### Francisco Kamilo

# Formatacao usando o Linux para alterar ordem do boot

No dia 26/10/2023 na aula de manutencao e suporte de computadores tivemos uma aula sobre como alterar a ordem do boot usando o linux. Professor pediu para quer conseguisse por o windows quando ligase o computador ja estivesse no windows. MBR: Um Master Boot Record, em portugues Registro Mestre de Inicializacao, e um tipo especial de setor de inicializacao no inicio de dispositivos de armazenamento em massa particionados de computadores, como discos fixos ou unidades removiveis destinadas para uso em sistemas compativeis com IBM PC e demais. GRUB: e mais uma alternativa como gerenciador de boot e apresenta alguns recursos extras com relacao as outras opcoes disponiveis. Ele e flexivel, funcional e poderoso, podendo inicializar sistemas operacionais como o Windows (9x, ME, NT, 2000 e XP), Dos, Linux, GNU Hurd, *BSD, OS/2 e etc. tambem como alterar a ordem do boot ubuntu:(CMD "Ctrl + Alt + t" para abrir o CMD no Ubuntu)
 GRUB - como alterar a ordem de boot
1. Edite o arquivo /etc/default/grub. sudo gedit /etc/default/grub.
2. Altere a linha GRUB_DEFAULT=0 para GRUB_DEFAULT=saved.
3. Salve o arquivo.
4. Atualize o Grub: sudo update-grub.
5. Escolha o SO default:
Mudando a ordem de boot no Ubuntu (ou similares) com GRUB 2:
1. Verifique no prompt do boot, qual a ordem do S.O. que voce quer.
Por exemplo: a primeira linha no prompt tem a ordem zero, a segunda 1 e assim por diante. Suponha que o S.O. selecionado esteja na ordem 5 (cinco).
2. Abra o arquivo, em /etc/default/grub:
 $ sudo gedit /etc/default/grub
3. Procure a linha:
GRUB_DEFAULT=0
E mude para:
GRUB_DEFAULT=5
Salve e feche o arquivo.
4. Depois, rode o comando:
sudo update-grub
Fake update: Onde mostra uma tela q o windows esta em atualicao.
Aplicativo que serve para instalar o windows em muitos PCS:
Para instalar o Windows em varios PCs, e comum usar o Microsoft Deployment Toolkit (MDT) ou o System Center Configuration Manager (SCCM). Essas ferramentas sao projetadas para implantacao e gerenciamento de sistemas operacionais, incluindo o Windows, em ambientes empresariais ou de grande escala.
O Microsoft Deployment Toolkit (MDT) e uma solucao gratuita da Microsoft que permite criar imagens personalizadas do Windows e automatizar o processo de implantacao. Com o MDT, voce pode implantar o Windows em varios computadores ao mesmo tempo e personalizar as instalacoes de acordo com suas necessidades.
O System Center Configuration Manager (SCCM) e uma solucao mais abrangente que vai alem da implantacao do sistema operacional e inclui gerenciamento de software, atualizacoes e muito mais. O SCCM e uma ferramenta poderosa, mas geralmente e usada em ambientes corporativos de medio a grande porte e pode ter custos associados.
Alem dessas opcoes, existem outras ferramentas de terceiros disponeveis no mercado que podem facilitar a implantacao do Windows em varios PCs. A escolha da ferramenta depende do tamanho e das necessidades da sua organizacao. Certifique-se de revisar as opcoes disponiveis e escolher a que melhor atende aos seus requisitos.
# AHCI: 
AHCI (Advanced Host Controller Interface) e uma especificacao de interface de hardware e software que permite que sistemas operacionais, como o Windows, comuniquem-se eficientemente com dispositivos de armazenamento, como discos rigidos e unidades de estado solido (SSDs) conectados a controladoras SATA (Serial Advanced Technology Attachment).
As principais caracteristicas e beneficios do AHCI incluem:
1. Hot-swapping: Permite a conexao e desconexao de dispositivos de armazenamento sem a necessidade de reiniciar o sistema, o que e util em ambientes de servidor e desktop.
2. Suporte a NCQ (Native Command Queuing): Isso permite que a controladora reorganize comandos de leitura e gravacao de maneira mais eficiente, melhorando o desempenho do disco.
3. Melhor gerenciamento de energia: O AHCI oferece recursos avancados de gerenciamento de energia, permitindo que os dispositivos entrem em estados de baixa energia quando nao estao em uso, economizando energia.
4. Suporte a discos opticos: O AHCI tambem e usado para discos opticos, como unidades de DVD e Blu-ray, o que possibilita o uso de unidades opticas de alta velocidade.
Em sistemas modernos, o AHCI e a configuracao padrao recomendada para controladoras SATA. No entanto, em algumas placas-mae mais antigas, voce pode encontrar a opcao de usar o modo IDE (Integrated Drive Electronics), que e uma interface mais antiga e menos eficiente em comparacao com o AHCI. Certos sistemas tambem oferecem o modo RAID (Redundant Array of Independent Disks) para criar matrizes de discos, mas esse modo geralmente inclui suporte ao AHCI.
Se voce estiver instalando um sistema operacional, como o Windows, e aconselhavel configurar a controladora SATA no modo AHCI para aproveitar todos os beneficios e recursos avancados que ele oferece. Certifique-se de verificar as configuracoes na BIOS ou UEFI do seu sistema para fazer essa selecao.
# Raid on:
 Parece que voce mencionou "Raid on", mas nao esta claro qual e o contexto ou a pergunta especifica relacionada a isso. "RAID" e a sigla para "Redundant Array of Independent Disks" (ou "Redundant Array of Inexpensive Disks"), que e uma tecnologia de armiazenamento que envolve a combinacao de varios discos rigidos para melhorar o desempenho, a confiabilidade ou a capacidade de armazenamento de dados. Existem diferentes niveis de RAID, como RAID 0, RAID 1, RAID 5, RAID 10, entre outros, cada um com suas proprias caracteristicas e usos.
Se voce tiver uma pergunta especifica sobre RAID ou precisar de informacoes adicionais, por favor, forneca mais detalhes para que eu possa ajudar de forma mais precisa.
# Refencias:
Bibliografia
Alterar a ordem de boot [RESOLVIDO]. Disponivel em: <https://www.vivaolinux.com.br/topico/vivaolinux/Alterar-a-ordem-de-boot>. Acesso em: 27 out. 2023.
fakeupdate.net - Installing Windows 10. Disponivel em: <https://fakeupdate.net/win11/>. Acesso em: 27 out. 2023.
GRUB. Disponivel em: <https://www.guiafoca.org/guiaonline/inicianteintermediario/ch06s02.html>. Acesso em: 27 out. 2023.
WIKIPEDIA CONTRIBUTORS. Master Boot Record. Disponivel em: <https://pt.wikipedia.org/w/index.php?title=Master_Boot_Record&oldid=66591806>.
Disponivel em: <https://chat.openai.com/c/fb64e38f-f9be-45e5-87c1-35508688e83e>. Acesso em: 27 out. 2023.