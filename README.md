# Slip_Coin_Stimulator
target_count=21
minimum_difference=2
heads_count=0
tails_count=0
flips_count=0
while((1))
do
     (( flips_count++))
     echo -n "Flip-$flips_count is"
     toss=$((RANDOM%2))
     if((toss==0))
     then
         echo "heads"
         ((heads_count++))
     else
         echo "tails"
         ((tails_count++))
fi

diff_bt_hc_tc=$((head_count - tail_count))
if(( heads_count == target_count && diff_bt_hc_tc >= minimum_difference))
      then
          echo "heads won by $diff_bt_hc_tc points"
          break
elif(( tail_count == target_count && ${diff-bt_hc_tc} >=minimum_difference))
      then
          echo "tails won by ${diff_bt_hc_tc}points"
      break
fi
done
echo"the head count is $heads_count tail count is $tails_count"
