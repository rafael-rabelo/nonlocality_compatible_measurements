# nonlocality_compatible_measurements
Supplementary data regarding the results presented in https://arxiv.org/abs/1806.09232 . In what follows, all concepts are properly defined and introduced in this reference.

The data is coded in MATLAB .mat files, each of which corresponding to a two-parameter family of two-qubit quantum states. The main contents of each file are the matricial forms of the measurements and states that lead to the critical points -- the critical values of $w$, as functions of $\alpha$, above which the states are capable of violating inequality 15 -- in the two plots presented.

The files are:
- Data_Horodecki_States.mat refers to the family introduced in equations (17), also referred to as Horodecki states;
- Data_Depolarized_Partially_Entangled_States.mat refers to the family introduced in equations (19).

Each file contains:
- Measurements: matlab cell (100x2x4). Entry Measurements{alpha_index,party,index} is a 8x8 matrix, corresponding to the dichotomic observable of the given index, party and alpha index.
- Measurements_qubit: matlab cell (100x2x4). Entry Measurements_qubit{alpha_index,party,index} is a 2x2 matrix, corresponding to the dichotomic observable of the given index, party and alpha index. Obtained from Measurements by means of suitable partial tracing on the remaining 'parties'.
- States: matlab cell (100x1). Entry States{alpha_index} is a 8x8 matrix, corresponding to the state of the system for the given alpha index, and associated critical $w$. The state is a two-qubit state embededded in $C^2 \otimes C^4$, written in the same basis as the measurements, fixed by the tensorial structure $C^4 = C^2 \otimes C^2$ where measurements 1 and 3 of Bob act on the first $C^2$ and measurements 2 and 4 of Bob act on the second $C^2$.
- alpha: matlab vector (100x1). Entry alpha(alpha_index) returns the value of $\alpha$ for the given alpha index.
- critical_w: matlab vector (100x1). Entry critical_w(alpha_index) returns the critical value of $w$ for the given alpha index.
