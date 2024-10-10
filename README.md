# DIO - Politicas de Acesso no Azure
 Gerenciando Politicas em Acessos Azure


## 🔎 Portal de Confiança do Serviço	

Acesse o site https://servicetrust.microsoft.com/ para verificar as certificações, regulamentos e padrões de serviço da Microsoft.

Esse site mostra os padrões de conformidade da Microsoft permitindo ter a comprovação em casos de auditoria, para que os clientes possam ver que a Microsoft segue as boas práticas.

![AZ09-01](https://github.com/user-attachments/assets/09fde404-f517-499c-a2fb-b1ba84941bde)

Ao clicar em qualquer um dos itens é possível acessar mais detalhes:

![AZ09-02](https://github.com/user-attachments/assets/8c3a4367-eeb1-4999-8b15-aa3f1e652e23)

![AZ09-03](https://github.com/user-attachments/assets/8d6c1953-31a8-480f-b29a-7776979d2083)

Note que é possível acessar documentos específicos de cada país, verificar a data de última atualização do documento e realizar o download:

![AZ09-04](https://github.com/user-attachments/assets/3d05bbcc-d646-4350-aa32-fa6abcf2f075)

![AZ09-05](https://github.com/user-attachments/assets/689ba2c2-a64e-40e9-9431-8bc605ac0889)


## Bloqueios no Azure

Abra o portal do [`Azure`](https://portal.azure.com), acesse o grupo de recursos criado e clique em **Locks**:

![AZ09-06](https://github.com/user-attachments/assets/8c3eccd2-0cab-4b09-a57a-a79b0d3b853e)

Essa funcionalidade permite adicionar um bloqueio a nível de resource group.

Clique em **+ Add**, preencha os campos necessários e clique em **OK** para criar um novo bloqueio:

![AZ09-07](https://github.com/user-attachments/assets/1fa5d0c1-efc6-40e9-8d03-6a7d50b521b0)

Foi criado então um bloqueio de exclusão para o grupo de recursos:

![AZ09-08](https://github.com/user-attachments/assets/baec4796-299a-467d-9eb1-1aecb4d71dfb)

Retorne e acesse um recurso do grupo de recursos:

![AZ09-09](https://github.com/user-attachments/assets/dca84230-2fab-4832-b5ae-d44ddfa4a346)

Clique em **Locks** e verifique que o escopo do bloqueio existente é referente ao grupo de recursos:

![AZ09-10](https://github.com/user-attachments/assets/9a4858ce-3bf1-4534-8bae-189da9e1f5a2)

Tente deletar o recurso e repare na mensagem que aparece:

![AZ09-11](https://github.com/user-attachments/assets/a5dbccb4-319a-4676-b110-9933ef7f6d12)

No mesmo recurso clique em **Move** e **Move to another resource group**:

![AZ09-12](https://github.com/user-attachments/assets/60643f01-f05c-4d7e-a4a7-ea60a3f3e5c0)

Selecione o grupo de recursos para onde ele será movido e clique em **Next**:

![AZ09-13](https://github.com/user-attachments/assets/c289a330-0b29-41e8-a1e1-9eaabc25cc25)

Aguarde a validação finalizar e clique em **Next**:

![AZ09-14](https://github.com/user-attachments/assets/b2ee43b6-5875-45ef-a053-3481760abefa)

Na próxima tela marque o campo indicado na imagem abaixo e clique em **Move**:

![AZ09-15](https://github.com/user-attachments/assets/7bbca844-3ced-4113-b6a0-0483a2175770)

Abra o grupo de recursos para onde ele foi movido e aguarde o recurso ser movido:

![AZ09-24](https://github.com/user-attachments/assets/7371220d-0208-45c0-8254-6ddde048e86a)

Abra o recurso que foi movido e clique em **Locks**, repare na mensagem de que não há bloqueios:

![AZ09-25](https://github.com/user-attachments/assets/993fbee9-31e3-4cac-9f95-67524a313090)

Dessa forma, os recursos movimentados de um grupo de recursos para outro não levam consigo os bloqueios do grupo de recursos de origem, e no grupo de recursos de origem o bloqueio permanece inalterado a não ser que seja excluído.

O bloqueio só irá com o recurso se for aplicado no próprio recurso.

Além disso, se for aplicado um bloqueio de somente leitura, não será possível realizar nenhuma ação no grupo de recursos ou no recurso onde esse bloqueio for aplicado, inclusive não será possível mover o recurso.


## Microsoft Purview

No portal do Azure pesquise por **Microsoft Purview**:

![AZ09-16](https://github.com/user-attachments/assets/00356623-7878-4fbf-a07f-90552d43e18e)

Esse é um recurso que precisa ser criado e administrado.

Para criar, clique em **+ Create**:

![AZ09-17](https://github.com/user-attachments/assets/4bed9829-d517-4006-8ad3-647eaa8a2b20)

Preencha os campos necessários em todas as abas e ao final clique em **Review + Create**:

![AZ09-18](https://github.com/user-attachments/assets/0c312f87-75bd-4edc-96d7-4f5cce797f0b)

Para acessar o portal do Microsoft Purview clique no usuário criado:

![AZ09-19](https://github.com/user-attachments/assets/b9037b5d-7a21-4dd9-a3c6-9023ff7ff6f5)

E após clique em **Open Microsoft Purview Governance Portal**:

![AZ09-20](https://github.com/user-attachments/assets/4d20c9df-448b-4533-9c70-37d1e73e0fc5)

O Microsoft Purview é uma suit de aplicações voltadas à segurança, governança e compliance para vários serviços da Microsoft, ajudando a identificar pontos fracos e pontos fortes relacionados à esses itens.

![AZ09-21](https://github.com/user-attachments/assets/358e5d9c-5f16-4ef9-b1d3-ca720e9a732a)

Repare nos recursos diponíveis e clique em **View all solutions**:

![AZ09-22](https://github.com/user-attachments/assets/17cbb40d-2076-454b-9fcb-36c81118be75)

Clique nas categorias para verificar os recursos relacionados a cada uma:

![AZ09-23](https://github.com/user-attachments/assets/a5c91fb2-d1f2-447e-a317-e826453bc085)


## Policies

No portal do Azure pesquise por **Policy**:

![AZ09-26](https://github.com/user-attachments/assets/0300b49b-8f9f-49af-a5a6-321465b54ca8)

Em **Overview** ele traz uma visão das politicas aplicadas ao ambiente da Azure em questão, onde 8 recursos estão de acordo com as regras de compliance e 1 não:

![AZ09-27](https://github.com/user-attachments/assets/b11c9d3b-dd07-47f0-bdc3-81a6297ff591)

Clique em uma das politicas:

![AZ09-28](https://github.com/user-attachments/assets/49a71e30-489e-437a-aa08-c8e99a1ed5c3)

Clique em **View assingment**:

![AZ09-29](https://github.com/user-attachments/assets/749286fb-eb49-42c1-b3fa-ddab2a7a73d6)

Clique em **Edit assingment** para visualizar as configurações da politica:

![AZ09-30](https://github.com/user-attachments/assets/d9237746-2a5f-4b12-9a4e-a18c00819519)

![AZ09-31](https://github.com/user-attachments/assets/5c835e5c-a0aa-4dbb-9c88-a834f076dce4)

Sendo que em *Scope* é selecionada qual assinatura do Azure irá receber as regras, em *policy definition* as regiões permitidas, e em *Assignment name* pode ser definido o nome da politica.

Os usuários podem criar politicas persolizadas e não se prender apenas às que já existem no portal.

Avance para a aba **Parameters** e repare nas regiões selecionadas, isso significa que qualquer recurso que tente ser criado fora dessas regiões não será permitido:

![AZ09-32](https://github.com/user-attachments/assets/e816a701-90f9-4e74-a3dd-03b32c3c1b15)

Se a politica fosse criada após já existirem recursos em áreas não permitidas, ela ficaria em não compliance, até que os recursos nessas áreas não permitidas fossem removidos.

Para criar uma nova politica clique em **Assignments**:

![AZ09-33](https://github.com/user-attachments/assets/48f76f3f-810f-4e1d-b481-0fc47a35e5dc)

Clique em **Assign policy**:

![AZ09-34](https://github.com/user-attachments/assets/aa60feec-b59b-4b93-bf63-ed601de6e273)

Clique no campo **Policy definition** e verifique a quantidade de politicas/regras já existentes:

![AZ09-35](https://github.com/user-attachments/assets/5631ab74-21ae-49ee-9a4a-bbbe80578798)

Repare que por padrão o botão de habilitação da nova politica já vem como *Enabled*, podendo ser alterado caso a politica ainda esteja em teste:

![AZ09-36](https://github.com/user-attachments/assets/3186db69-5dcb-44bd-b7e5-37a320d6ce0b)

Outro detalhe sobre as politicas é que elas são aplicadas à assinatura do Azure como um todo, e funciona da mesma forma para todos os usuários independente de qual seja seu nível hierárquico na empresa.


## Links utilizados

- https://servicetrust.microsoft.com/

- https://portal.azure.com
