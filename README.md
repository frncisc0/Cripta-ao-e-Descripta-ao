#  Tutorial de Criptografia Básica com Ccrypt no Kali Linux
Sugestão de Estrutura e Redação para o README
Título: Tutorial de Criptografia Básica com Ccrypt no Kali Linux

Introdução:

Este tutorial demonstra passo a passo como criptografar e descriptografar arquivos utilizando a ferramenta Ccrypt em um ambiente Kali Linux. A criptografia é um processo fundamental para proteger dados sensíveis e prevenir acessos não autorizados.

Pré-requisitos:

Uma máquina virtual com Kali Linux instalada.
Conhecimento básico de linha de comando.
Passo a Passo:

1 Ativando o Modo Superusuário:

sudo su
Ao executar este comando, você obtém privilégios de administrador, necessários para instalar e utilizar o Ccrypt.

![Captura de tela 2024-12-18 213104](https://github.com/user-attachments/assets/cfa333b6-3e92-44b0-a98c-206095940789)

2 Instalando o Ccrypt:

apt install ccrypt
Com este comando, o Ccrypt será instalado em seu sistema, fornecendo as ferramentas necessárias para a criptografia.

![Captura de tela 2024-12-18 213213](https://github.com/user-attachments/assets/a976004d-dcad-42d6-ae60-2c39ef6b13b6)

3 Criando um Arquivo:

nano teste.txt
Crie um arquivo de texto simples chamado "teste.txt" e adicione o conteúdo desejado.

![Captura de tela 2024-12-18 213213](https://github.com/user-attachments/assets/783dbe1d-36df-4af0-86c8-e910e38d3dfc)

![Captura de tela 2024-12-18 213331](https://github.com/user-attachments/assets/68f5e63e-49e9-4799-8270-058cdaecbac8)

4 Criptografando o Arquivo:

ccrypt teste.txt
Ao executar este comando, o Ccrypt solicitará uma senha. Digite e confirme a senha escolhida. O arquivo original será substituído por um arquivo com a extensão ".cpt", que contém os dados criptografados.

![Captura de tela 2024-12-18 213521](https://github.com/user-attachments/assets/f53f0f6c-b121-4684-a463-1ba137154954)

5 Verificando o Arquivo Criptografado:

ls
Liste os arquivos no diretório para confirmar que o arquivo original foi substituído pelo arquivo criptografado.

6 Abrindo o arquivo Criptografado:

nano teste.txt.cpt
Tente abrir o arquivo criptografado. Você verá caracteres aleatórios, indicando que o conteúdo está seguro.

![Captura de tela 2024-12-18 213554](https://github.com/user-attachments/assets/e67de905-c084-46d6-9445-9ddbfe13ef3d)

7 Alterando a Senha:

ccrypt -x teste.txt.cpt
Este comando permite alterar a senha do arquivo criptografado. Siga as instruções para inserir a senha antiga e a nova senha.

![Captura de tela 2024-12-18 213929](https://github.com/user-attachments/assets/e2c8fd84-9f13-424b-bc08-bff080792f10)

8 Descriptografando o Arquivo:

ccrypt -d teste.txt.cpt
Digite a senha correta para descriptografar o arquivo. O arquivo original será restaurado.

![Captura de tela 2024-12-18 214118](https://github.com/user-attachments/assets/3846fbeb-883f-4fd5-9d8e-44bed58d0dbe)

![Captura de tela 2024-12-18 214201](https://github.com/user-attachments/assets/969d3cd0-8e3d-4774-80e3-a2b600149426)

Considerações:

Segurança da Senha: Utilize senhas fortes e únicas para cada arquivo criptografado.
Armazenamento da Chave: Guarde a senha em um local seguro, pois sem ela não é possível descriptografar o arquivo.
Outros Algoritmos: O Ccrypt oferece suporte a diversos algoritmos de criptografia. Consulte a documentação para mais informações.
Observação: Este tutorial tem como objetivo educacional e demonstra uma forma básica de criptografia. Para aplicações mais complexas, considere utilizar ferramentas e técnicas mais avançadas.
