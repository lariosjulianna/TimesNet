# TimesNet
Unfinished

Clone repo

in terminal, run

model_name=times_net python -u run.py \
--task_name short_term_forecast \
--is_training 1 \
--root_path ./dataset/ \
--data_path BTD.txt \
--model_id BTD_96_96 \
--model times_net \
--data BTD \
--features M \
--seq_len 96 \
--label_len 48 \
--pred_len 96 \
--e_layers 2 \
--d_layers 1 \
--factor 3 \
--enc_in 5 \
--dec_in 5 \
--c_out 5 \
--d_model 16 \
--d_ff 32 \
--des 'Exp' \
--itr 1 \
--top_k 5

# There are errors!
Need to debug data_loader

Main issue is changing it to reflect time series with the given data
TimesNet model orignally uses Date, Day, Hour, Minute
Our data only has Tree_type, Bone_ID, Frame_ID, x, y, and z.
