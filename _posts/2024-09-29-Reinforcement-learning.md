---
layout: post
read_time: true
show_date: true
title:  Markov Decision Process
date:   2024-09-29
description: Process to solve Sequential Decision
img:  posts/20210228/MLLibrary.jpg 
tags: [RL, coding]
author: 
github:  
mathjax: yes
---
## Markov

### 1. 마르코프 프로세스
$MP \equiv(S,P) $  

미리 정의된 어떤 확률 분포를 따라서 상태와 상태 사이를 이동하는 여정  

- S: 상태의 집합
- P: 전이 확률 행렬

### 2. 마르코프 성질
$\mathbb{P}[S_{t+1}|S_t] = \mathbb{P}[S_{t+1}|S_1,S_2,...,S_t]$  

미래는 오로지 현재에 의해 결정된다  

$\mathbb{P}[S_{t+1}|S_t] = \mathbb{P}[S_{t+1}|S_1,S_2,...,S_t]$

- 마르코프하지 않은 상태이어도 이전 상태를 엮어서 상태를 제공하면 마르코프 성질을 만족시킬 수 있다.

> (Human-level control through deep reinforcement learning 2015)

### 3. 마르코프 리워드 프로세스
$MRP \equiv(S,P,R,\gamma)$

MP에 보상개념을 추가  

- R: 보상 함수  
$R = E[R_t|S_t = s]$

- $\gamma$ (감쇠 인자): 당장 얻는 보상을 얼마나 중요시 할 것인지를 나타내는 파라미터.  
만약 $\gamma$가 0이면 미래의 보상이 모두 무시되므로 근시안적인 에이전트가 됨. 1이면 매우 장시안적. 1보다 작게 해주면  return이 무한해지는 것을 방지할 수 있다.(무한해지면 어느 경우가 더 나은지 판단못함)

- $G_t$ (Return): 현재부터 미래에 얻게 될 보상의 합. 과거의 보상은 고려안함.

- 에피소드: 하나의 여정

#### Monte-Carlo 접근법
실제 확률을 잘 모를 경우 샘플링을 통해 어떤 값을 유추하는 방법론

#### 상태 가치 함수(State Value Function)
$V(S) = E[G_t|S_t=s]$

- 상태의 가치 평가는 리턴의 기대값을 사용
- 에피소드마다 리턴이 다르므로 기대값을 이용해서 정의.
- 시점 t에서 상태s부터 시작하여 에피소드가 끝날 때까지의 리턴을 계산. but 에피소드가 무한할 때는 샘플로 얻은 리턴의 평균을 통해 근사하게 계산.

### 4. 마르코프 결정 프로세스
$MDP \equiv(S,A,P,R,\gamma)$  

MRP에 에이전트가 더해짐  

- A: 에이전트가 취하는 액션의 집합
- P: 상태S에서 액션a를 선택할 때 상태S'가 될 확률  
    $P_{ss'}^a = P[S_{t+1} = s'|S_t=s, A_t = a]$

상태가 결정론적이 아니므로 같은 상태와 같은 액션을 선택해도 매번 다른 상태에 도착할 수 있다.
- R: 상태s에서 액션a를 선택하면 받는 보상. 확률적으로 매번 바뀌기 때문에 기대값 이용.  
    $R_{s}^a = E[R_{t+1}|S_t=s, A_t = a]$

 - 정책: 보상의 합을 최대로 하는 전략. 어떤 액션을 선택할지 결정.  
 $\pi(a|s)=P[A_t=a|S_t=s]$  
 정책함수는 에이전트 안에 존재. 즉 환경에는 상태별 액셜 선택에 대한 확률이 없음. 이는 환경은 변하지 않지만 에이전트는 자신의 정책을 더 나은 보상을 받기 위해 언제든 교정해 나갈 수 있음을 의미.

#### 상태 가치 함수
: 정책함수에 의존적. 정책 고정.  
$v_\pi(S)=E_\pi[r_{t+1} + \gamma r_{t+2} + \gamma^2r_{t+3}+ ...|S_t=s]$  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$=E[G_t|S_t=s]$

#### 액션 가치 함수
각 상태에서 선택 가능한 모든 액션을 평가  
$q_\pi(s,a)=E_\pi[G_t|S_t=s, A_t=a]$
 
#### MDP의 목적
$v^*$ (최적 가치 함수): 최적 정책 $\pi^*$를 따를 때의 가치 함수 

- Prediction: 정책이 주어졌을 때 각 상태의 밸류를 평가
- Control: 최적 정책을 찾기

