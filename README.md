# AWS Auto Scaling: Elasticidade e Alta Disponibilidade

Este repositório documenta um laboratório prático focado na implementação de arquiteturas resilientes na AWS usando **Auto Scaling Groups (ASG)** e **Elastic Load Balancing (ELB)**.

## 🏗️ Arquitetura do Projeto
O objetivo foi criar um ambiente capaz de escalar horizontalmente de forma automática com base na utilização de CPU.

- **Frontend/Application:** Servidor web simples.
- **Compute:** Instâncias EC2 gerenciadas por um ASG.
- **Load Balancer:** Distribuição de tráfego entre múltiplas zonas de disponibilidade (us-west-2a e us-west-2b).
- **Automation:** Escalabilidade baseada em política de CPU (> 50%).

## 🚀 Etapas Executadas
1. **Definição de Imagem:** Criação de uma *Golden AMI* para padronização.
2. **Infraestrutura como Código (Conceitual):** Utilização de *Launch Templates* para garantir consistência nas novas instâncias.
3. **Configuração de ASG:** Definição de limites (Min: 2, Max: 4) e políticas de escalonamento.
4. **Stress Test:** Simulação de alta carga para validação da resposta automática do sistema.
5. **Monitoramento:** Observação da transição de estado no CloudWatch e provisionamento automático no EC2.

## 📊 Resultados
O sistema demonstrou capacidade de *Scale-Out* (adição de instâncias) em menos de 5 minutos após a detecção de alta carga, garantindo que a aplicação permanecesse disponível e performática.

---
*Este laboratório faz parte da minha jornada de aprendizado em AWS Cloud Computing.*
