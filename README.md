# Guia de Estudos e Anotações sobre Microsoft Azure - Criação de Máquina Virtual

## Descrição do Desafio

Este repositório documenta o processo de aprendizado e prática da criação e configuração de uma máquina virtual na plataforma Microsoft Azure, conforme proposto no laboratório do desafio. O objetivo é consolidar o conhecimento adquirido e criar um material de apoio para estudos futuros e implementações.

## Objetivos de Aprendizagem

Ao concluir este desafio, fui capaz de:

* Compreender os diferentes modelos de nuvem (pública, privada e híbrida) e suas características.
* Analisar os pontos positivos e negativos de cada modelo de nuvem.
* Identificar e descrever os principais pilares da nuvem Azure: escalabilidade, elasticidade, confiabilidade, previsibilidade, segurança, governança e gerenciabilidade.
* Realizar o passo a passo para a criação de uma máquina virtual utilizando o portal do Microsoft Azure.
* Documentar processos técnicos de forma clara e estruturada.
* Utilizar o GitHub como ferramenta para compartilhamento de documentação técnica.

## Modelos de Nuvem: Pública, Privada e Híbrida

Durante as aulas, aprendi sobre os três principais modelos de nuvem e suas distinções:

### Nuvem Pública

* **Definição:** Infraestrutura de computação pertencente a um provedor de serviços de nuvem de terceiros e compartilhada por vários clientes (organizações ou indivíduos). Exemplos incluem o Azure, AWS e GCP.
* **Pontos Positivos:**
    * **Custo-benefício:** Geralmente não há necessidade de grandes investimentos iniciais em hardware. O modelo de pagamento é geralmente "pelo uso".
    * **Escalabilidade:** Facilidade para aumentar ou diminuir recursos conforme a demanda.
    * **Manutenção:** O provedor é responsável pela manutenção e gerenciamento da infraestrutura.
    * **Acessibilidade:** Acesso aos recursos de qualquer lugar com conexão à internet.
* **Pontos Negativos:**
    * **Segurança:** Embora os provedores invistam fortemente em segurança, a natureza compartilhada pode gerar preocupações para alguns.
    * **Personalização:** Menos flexibilidade para personalizar a infraestrutura de acordo com necessidades muito específicas.
    * **Conformidade:** Em alguns casos, pode haver desafios para atender a requisitos de conformidade regulatória específicos.

### Nuvem Privada

* **Definição:** Infraestrutura de computação utilizada exclusivamente por uma única organização. Pode ser hospedada no data center da própria empresa ou por um provedor terceirizado.
* **Pontos Positivos:**
    * **Segurança:** Maior controle sobre a segurança e privacidade dos dados.
    * **Personalização:** Flexibilidade para adaptar a infraestrutura às necessidades específicas da organização.
    * **Conformidade:** Facilidade para atender a requisitos regulatórios específicos.
* **Pontos Negativos:**
    * **Custo:** Requer investimento inicial significativo em hardware e software, além dos custos de manutenção.
    * **Escalabilidade:** A escalabilidade pode ser mais limitada e exigir planejamento e investimento adicionais.
    * **Manutenção:** A organização é responsável pela manutenção e gerenciamento da infraestrutura (ou paga um provedor para isso).

### Nuvem Híbrida

* **Definição:** Combinação de nuvem pública e privada, permitindo que dados e aplicativos sejam compartilhados entre elas.
* **Pontos Positivos:**
    * **Flexibilidade:** Permite escolher o ambiente mais adequado para cada tipo de carga de trabalho.
    * **Escalabilidade:** Possibilidade de usar a nuvem pública para picos de demanda (cloud bursting).
    * **Controle:** Mantém dados sensíveis em um ambiente privado enquanto aproveita os benefícios da nuvem pública.
* **Pontos Negativos:**
    * **Complexidade:** O gerenciamento de um ambiente híbrido pode ser mais complexo.
    * **Integração:** Garantir a integração perfeita entre os ambientes público e privado pode ser um desafio.
    * **Custo:** Pode envolver custos tanto da infraestrutura privada quanto dos serviços da nuvem pública.

## Pilares da Nuvem Azure

As aulas também abordaram os pilares fundamentais que sustentam a nuvem Azure:

* **Escalabilidade:** Capacidade de aumentar ou diminuir os recursos de computação (como poder de processamento, armazenamento e largura de banda) de forma rápida e fácil para lidar com variações na demanda.
* **Elasticidade:** Semelhante à escalabilidade, mas geralmente se refere à capacidade de alocar e desalocar recursos automaticamente em resposta a mudanças em tempo real na demanda, otimizando custos.
* **Confiabilidade:** Capacidade do sistema de operar sem falhas e se recuperar rapidamente de interrupções, garantindo a continuidade dos negócios. Isso envolve redundância, backups e recuperação de desastres.
* **Previsibilidade:** Capacidade de prever e gerenciar os custos da nuvem de forma eficaz. O Azure oferece ferramentas e modelos de preços para ajudar os usuários a entender e controlar seus gastos.
* **Segurança:** Implementação de medidas e tecnologias para proteger dados, aplicativos e a infraestrutura contra ameaças e acesso não autorizado. A Azure oferece uma ampla gama de serviços e políticas de segurança.
* **Governança:** Estabelecimento de políticas, processos e controles para gerenciar e monitorar os recursos da nuvem, garantindo conformidade, segurança e otimização de custos.
* **Gerenciabilidade:** Facilidade com que os recursos da nuvem podem ser implantados, monitorados, gerenciados e mantidos. O Azure fornece diversas ferramentas e interfaces para simplificar essas tarefas.

## Tutorial Básico: Criando uma Máquina Virtual no Azure

Este é um breve tutorial dos passos básicos para criar uma máquina virtual (VM) usando o portal do Microsoft Azure:

1.  **Acesse o Portal do Azure:** Abra seu navegador e vá para [https://portal.azure.com/](https://portal.azure.com/). Faça login com sua conta Azure.
2.  **Criar um Recurso:** No menu principal ou na página inicial, clique em **"+ Criar um recurso"**.
3.  **Selecionar Computação:** Na barra de pesquisa, digite "Máquina Virtual" e pressione Enter. Selecione **"Máquina Virtual"** nos resultados.
4.  **Criar:** Na página de "Máquina Virtual", clique em **"Criar"** e selecione **"Máquina Virtual"** novamente.
5.  **Configurações Básicas:**
    * **Grupo de recursos:** Selecione um grupo de recursos existente ou crie um novo para organizar sua VM e outros recursos relacionados.
    * **Nome da máquina virtual:** Escolha um nome exclusivo para sua VM.
    * **Região:** Selecione a região do Azure onde você deseja hospedar sua VM (escolha uma região próxima aos seus usuários para menor latência).
    * **Opções de disponibilidade:** Escolha opções de redundância para garantir a disponibilidade da sua VM (para aprendizado, "Nenhuma redundância de infraestrutura necessária" pode ser suficiente).
    * **Imagem:** Selecione o sistema operacional que você deseja para sua VM (ex: Ubuntu Server, Windows Server).
    * **Tamanho:** Escolha o tamanho da VM que atenda às suas necessidades de computação, memória e disco. O Azure oferece diversas opções com diferentes custos.
6.  **Conta de Administrador:**
    * **Tipo de autenticação:** Escolha entre "Senha" ou "Chave pública SSH" para autenticação. Se escolher "Senha", defina um nome de usuário e uma senha segura. Se escolher "Chave pública SSH", você precisará fornecer sua chave pública.
7.  **Discos:**
    * Configure os discos para sua VM. O Azure geralmente sugere um disco de sistema operacional padrão. Você pode adicionar discos de dados conforme necessário.
8.  **Rede:**
    * O Azure criará ou permitirá que você selecione uma rede virtual e uma sub-rede.
    * **Grupo de segurança de rede (NSG):** Configure regras de firewall para controlar o tráfego de entrada e saída da sua VM (por exemplo, permitir tráfego na porta 22 para SSH ou porta 80 para HTTP).
9.  **Gerenciamento (Opcional):**
    * Configure opções como diagnóstico de inicialização, identidade gerenciada e outras configurações de gerenciamento.
10. **Avançado (Opcional):**
    * Configure extensões, dados personalizados e outras configurações avançadas.
11. **Tags (Opcional):**
    * Adicione tags para organizar e categorizar seus recursos do Azure.
12. **Revisar + criar:** Revise todas as suas configurações e clique em **"Criar"**.
13. **Implantação:** O Azure iniciará a implantação da sua máquina virtual. Você poderá acompanhar o progresso no painel de notificações.
14. **Conectar:** Após a implantação ser concluída, você poderá se conectar à sua VM usando SSH (para Linux) ou Conexão de Área de Trabalho Remota (RDP) para Windows, dependendo das suas configurações de rede e segurança.

## Conclusão

Este guia resume os principais conceitos aprendidos sobre a nuvem Azure e detalha os passos para a criação de uma máquina virtual. A prática e a documentação são etapas cruciais no processo de aprendizado e espero que este material sirva como um bom ponto de partida para futuras explorações no universo da computação em nuvem com o Azure.
