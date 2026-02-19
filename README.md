# Bell State

> **Category**: fundamentals &nbsp;|&nbsp; **Difficulty**: beginner &nbsp;|&nbsp; **Qubits**: 2 &nbsp;|&nbsp; **Gates**: 2 &nbsp;|&nbsp; **Depth**: 2

The Bell state is the simplest example of quantum entanglement. A Hadamard gate places qubit 0 in superposition, and a CNOT gate creates correlation between the two qubits. Measuring one qubit instantly determines the outcome of measuring the other, regardless of distance.

## Expected Output

50% |00⟩, 50% |11⟩

## Circuit

The OpenQASM 2.0 circuit is in [`circuit.qasm`](./circuit.qasm).

```
OPENQASM 2.0;
include "qelib1.inc";
qreg q[2];
creg c[2];
h q[0];
cx q[0],q[1];
measure q[0] -> c[0];
measure q[1] -> c[1];
```

## Tags

`entanglement` `fundamentals` `bell-state` `two-qubit`

## References

- [Nielsen & Chuang: Quantum Computation and Quantum Information, §1.3](https://doi.org/10.1017/CBO9780511976667)

## License

MIT — part of the [OpenQC Algorithm Catalog](https://github.com/openqc-algorithms).
