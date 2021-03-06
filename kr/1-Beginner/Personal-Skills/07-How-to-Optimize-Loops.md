# 루프를 최적화하는 법
[//]: # (Version:1.0.0)
때로 당신은 제품에서 실행하는 데에 오랜 시간이 걸리거나 병목 현상을 일으키는 루프들(loops)이나 재귀 함수를 마주칠 것입니다. 루프를 좀 더 빠르게 만드는 시도를 하기 전에, 그것을 완전히 없앨 방법이 있는지 몇 분 동안 생각해 보세요. 다른 알고리즘을 사용하면 어떨까요? 다른 것을 계산하는 동안 그것을 동시에 계산할 수 있을까요? 이러한 방법으로도 해결할 수 없다면, 그때 루프를 최적화하면 됩니다. 간단한 이야기입니다; 잡동사니들을 치워버리세요. 이는 결국 정교함과 더불어 각종 구문(statement)과 식(expression)의 비용에 대한 이해를 요구할 것입니다. 여기 몇 가지 제안이 있습니다:

- 부동 소수점 연산을 제거하세요.
- 불필요하게 새로운 메모리 블록을 할당하지 마세요.
- 상수의 연산은 미리 합니다(자세한 내용은 'constant folding' 키워드를 참고하세요 - `옮긴이`)
- I/O를 버퍼 안으로 옮깁니다.
- 나누기 연산을 피합니다. 
- 연산하는 데 리소스를 많이 사용하는 형 변환(typecasts)을 피합니다. 
- 인덱스를 다시 연산하는 대신 포인터를 옮깁니다.

이러한 각 연산들의 비용은 당신이 사용하는 특정 시스템에 따라 달라집니다. 어떤 시스템에서는 컴파일러와 하드웨어가 당신을 대신해서 이러한 것들을 처리해줍니다. 명료하고 효율적인 코드가 특정한 플랫폼에 대한 이해가 필요한 코드보다 낫습니다. 

다음 장 [I/O 비용을 다루는 법](06-How-to-Deal-with-IO-Expenses.md)
