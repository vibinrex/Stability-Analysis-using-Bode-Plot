# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:

![WhatsApp Image 2025-11-27 at 22 09 01_7c3f6a55](https://github.com/user-attachments/assets/2e89c0bb-9d3f-4d67-aa3c-71ff28cadf05)

![WhatsApp Image 2025-11-27 at 22 09 01_8c492519](https://github.com/user-attachments/assets/ae9e8ff7-8ddf-453e-8201-19981a1bf685)


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```
## Output:

<img width="1771" height="881" alt="image" src="https://github.com/user-attachments/assets/bcd4982a-7c0c-46f0-a33b-238e531e013e" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12<br>
Phase Margin = 60.4231<br>
Gain crossover frequency = 0.9070<br>
Phase crossover frequency = 4.4721<br>
The system is stable
