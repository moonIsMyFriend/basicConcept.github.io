---
layout: post
read_time: true
show_date: true
title:  Planning
date:   2024-09-29
description: Planning
img: posts/20210210/Game_of_Life.jpg
tags: [RL, coding]
author: 
github:  
mathjax: yes
---


##  1. 작은 문제, MDP를 안다.

- Planning: MDP에 대한 보상함수와 전이 확률을 알고 작은 문제인 경우 이를 이용하여 정책을 개선해 나가는 과정
- 테이블 기반 방법론(tabular method): 모든 상태 혹은 상태와 액션의 페어에 대한 테이블을 만들서 값을 업데이트하는 방식


### (1) Predication
- 반복적 정책 평가(iterative policy evaluation): 테이블의 값들을 초기화한 후, 벨만 기대 방정식을 반복적으로 사용하여 테이블의 값을ㄹ 조금씩 갱신하는 방법

### (2) Control (최고의 정책 찾기)
- 정책 이터레이션: 정책 평가와 정책 개선을 번갈아가며 정책이 수렴할 때까지 반복하는 방법론. 최고의 정책을 찾는 것이 목적이므로 정확한 가치를 평가는 것이 목적이 아님.
- 밸류 이터레이션: 최적 정책을 따랐을 때 나오는 최적 밸류에 초점. 벨만 최적 방정식을 이용.

## 2. 작은 문제, MDP 모름
- 모델 프리: 액션을 취하기 전에 는 보상도 액션에 대한 확률 분포도 모름
- 테이블 룩업: 테이블에 값을 기록하며 조금씩 갱신하는 방식

(1) 몬테카를로 학습
- 직접 측정하기 어려운 통계량을 샘플링을 통해 그 값을 가늠하는 기법(ex: MCTS, MCMC 등)
(2) Temporal difference

