# Three-AUVs-acoustic-communication-data
Ground truth AUV data collected Chesapeake bay area

The .mat data is constructed as follows:

# AUV A,B,C trajectories in NED
AUV_A_locArray_1.mat / AUV_B_locArray_1.mat / AUV_C_locArray_1.mat record three AUV ground truth positions in North East Down(NED) coordinates
.mat data file has three columns:
| N | E | D |


# AUV A,B,C successful communications
A_send_B_rece_suc_pack_1.mat / A_send_C_rece_suc_pack_1.mat / B_send_A_rece_suc_pack_1.mat / B_send_C_rece_suc_pack_1.mat / C_send_A_rece_suc_pack_1.mat / C_send_B_rece_suc_pack_1.mat record successful communication events. For exmaple A_send_B_rece_suc_pack_1.mat records all successful communications sending from AUV A to AUV B.

.mat data file has ten columns:

| sending_time_unix | receiving_time_unix | sending_position_N | sending_position_E | sending_position_D | receiving_position_N | receiving_position_E | receiving_position_D | distance | label |
where distance is ground truth distance between sending and receiving AUV when event happens and label = 1 represents successful event



# AUV A,B,C unsuccessful communications
A_send_B_rece_unsuc_pack_1.mat / A_send_C_rece_unsuc_pack_1.mat / B_send_A_rece_unsuc_pack_1.mat / B_send_C_rece_unsuc_pack_1.mat / C_send_A_rece_unsuc_pack_1.mat / C_send_B_rece_unsuc_pack_1.mat record unsuccessful communication events. For exmaple A_send_B_rece_unsuc_pack_1.mat records all unsuccessful communications sending from AUV A to AUV B.

.mat data file has nine columns:

| sending_time_unix | sending_position_N | sending_position_E | sending_position_D | receiving_position_N | receiving_position_E | receiving_position_D | distance | label |

where distance is ground truth distance between sending and receiving AUV when event happens and label = 0 represents unsuccessful event



