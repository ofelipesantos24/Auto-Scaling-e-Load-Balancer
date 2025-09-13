# Projeto: Auto Scaling, Load Balancer e Regras de Scaling

## 🔹 O que é cada um?
- **Auto Scaling**  
  Serviço que ajusta automaticamente a quantidade de instâncias de acordo com a demanda. Ele cria ou remove recursos sem precisar de intervenção manual.  

- **Load Balancer**  
  É o distribuidor de tráfego. Ele recebe as requisições dos usuários e envia para diferentes instâncias, evitando sobrecarga em apenas uma.  

- **Regras de Scaling Up/Down**  
  - **Scaling Up (scale out)** → aumentar a quantidade de instâncias quando a demanda sobe (ex: CPU > 70%).  
  - **Scaling Down (scale in)** → reduzir a quantidade de instâncias quando a demanda cai (ex: CPU < 30%).  

---

## 🔹 O que aprendemos
- A importância de **não depender de apenas uma instância**, pois ela pode falhar.  
- Que o **balanceamento** melhora o desempenho e disponibilidade.  
- Que o **Auto Scaling economiza recursos**: só usa mais instâncias quando realmente precisa.  
- Como criar **regras de métricas** (CPU, memória, tráfego, etc.) para deixar o processo automático.  

---

## 🔹 Passo a passo de cada serviço

### 1. Auto Scaling
1. Criar um grupo de Auto Scaling (ASG).  
2. Definir a quantidade mínima, máxima e desejada de instâncias.  
3. Vincular ao Load Balancer para distribuir o tráfego.  
4. Configurar as políticas de scaling (up e down).  

### 2. Load Balancer
1. Criar um Load Balancer.  
2. Definir as zonas de disponibilidade.  
3. Criar target groups (grupos de instâncias).  
4. Associar o Auto Scaling Group ao Load Balancer.  

### 3. Regras de Scaling Up/Down
1. Escolher as métricas de monitoramento (ex: CPU).  
2. Definir limites de uso (thresholds).  
3. Criar política de **Scale Out** (ex: adicionar 1 instância se CPU > 70%).  
4. Criar política de **Scale In** (ex: remover 1 instância se CPU < 30%).  

---
