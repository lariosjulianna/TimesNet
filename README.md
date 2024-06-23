# TimesNet
Unfinished!

1.
   Clone repo

2. 
   in terminal, run first script in TimesNet_M4.sh
OR
model_name=times_net
python -u run.py \
  --task_name short_term_forecast \
  --is_training 1 \
  --root_path ./dataset/BTD \
  --seasonal_patterns 'Hourly' \
  --model_id BTD_Hourly \
  --model $model_name \
  --data BTD \
  --features M \
  --e_layers 2 \
  --d_layers 1 \
  --factor 3 \
  --enc_in 1 \
  --dec_in 1 \
  --c_out 1 \
  --batch_size 16 \
  --d_model 32 \
  --d_ff 32 \
  --top_k 5 \
  --des 'Exp' \
  --itr 1 \
  --learning_rate 0.001 \
  --loss 'SMAPE'
  
# There are errors!
3.
  File "run.py", line 166, in <module>
    exp = Exp(args)  # set experiments
  File "/csse/users/jla256/timesnet-env/timesnet/exp/exp_short_term_forecasting.py", line 22, in __init__
    super(Exp_Short_Term_Forecast, self).__init__(args)
  File "/csse/users/jla256/timesnet-env/timesnet/exp/exp_basic.py", line 40, in __init__
    self.model = self._build_model().to(self.device)
  File "/csse/users/jla256/timesnet-env/timesnet/exp/exp_short_term_forecasting.py", line 30, in _build_model
    model = self.model_dict[self.args.model].Model(self.args).float()
TypeError: __init__() missing 2 required positional arguments: 'label_len' and 'pred_len'
