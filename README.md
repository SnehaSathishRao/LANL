# LANL
**Business problem:**  
The goal of the challenge is to capture the physical state of the laboratory fault and how close it is from failure from a snapshot of the seismic data it is emitting. We will have to build a model that predicts the time remaining before failure from a chunk of seismic data.

**Features:**  
* acoustic_data - the seismic signal [int16]
* time_to_failure - the time (in seconds) until the next laboratory earthquake [float64]
* seg_id - the test segment ids for which predictions should be made (one prediction per segment)

**Machine Learning Problem:**  
This is a regression problem which predicts time_to_failure. 
MAE is used as a performance metric.

**Summary:**

+-------------------+-----------+----------------------+
|       Model       | parameter |         MAE          |
+-------------------+-----------+----------------------+
| Linear Regression |    0.01   | 2.96480436810495e+20 |
|   Random Forest   |  [20, 5]  |  1.9564757699852753  |
|        SVR        |     2     |  1.9602751207861904  |
|         XG        |  [30, 5]  |  2.073588029812832   |
+-------------------+-----------+----------------------+
