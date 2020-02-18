# Project1_Glenn

    import pandas as pd
    import numpy
    import numpy as np
    import math
    import pylab
    import matplotlib as plt
    import matplotlib.pyplot as plt
    from pandas import DataFrame, Series
    import matplotlib.patches as mpatches
    from pylab import plot, ylim, xlim, show, xlabel, ylabel, grid

# Reading All the Data


    df_W1=pd.read_csv('OregonShelfSurfacePiercingProfilerMooringWinter.csv')
    df_S1=pd.read_csv('OregonShelfSurfacePiercingProfilerMooringSummer.csv')

    df_W2=pd.read_csv('OregonOffshoreCabledShallowProfilerMooringWinter.csv')
    df_S2=pd.read_csv('OregonOffshoreCabledShallowProfilerMooringSummer.csv')

    df_W3=pd.read_csv('OregonOffshoreCabledDeepProfilerMooringWinter.csv')
    df_S3=pd.read_csv('OregonOffshoreCabledDeepProfilerMooringSummer.csv')

    df_W4=pd.read_csv('OregonSlopeBaseShallowProfilerWinter.csv')
    df_S4=pd.read_csv('OregonSlopeBaseShallowProfilerSummer.csv')

    df_W5=pd.read_csv('OregonSlopeBaseDeepProfilerWinter.csv')
    df_S5=pd.read_csv('OregonSlopeBaseDeepProfilerSummer.csv')

    df_W6=pd.read_csv('AxialBaseShallowProfilerWinter.csv')
    df_S6=pd.read_csv('AxialBaseShallowProfilerSummer.csv')

    df_W7=pd.read_csv('AxialBaseDeepProfilerWinter.csv')
    df_S7=pd.read_csv('AxialBaseDeepProfilerSummer.csv')

# Defining Variables

# First data set

    PW1=df_W1.pressure
    TW1=df_W1.temperature
    SW1=df_W1.salinity
    TW1_2 = TW1*TW1
    TW1_3 = TW1*TW1*TW1
    cW1 = (1449.2 + (4.6 * TW1) - (.055 * TW1_2) + (.00029 * TW1_3) + ((1.34 - 0.01*TW1)*(SW1 - 35)) + (.016*PW1))
    timeW1 = df_W1.time

    PS1=df_S1.pressure
    TS1=df_S1.temperature
    SS1=df_S1.salinity
    TS1_2 = TS1*TS1
    TS1_3 = TS1*TS1*TS1
    cS1 = (1449.2 + (4.6 * TS1) - (.055 * TS1_2) + (.00029 * TS1_3) + ((1.34 - 0.01*TS1)*(SS1 - 35)) + (.016*PS1))
    timeS1 = df_S1.time

    yW1 = PW1
    xW1 = cW1
    yS1 = PS1
    xS1 = cS1

# Second data set

    PW2=df_W2.seawater_pressure
    TW2=df_W2.seawater_temperature
    SW2=df_W2.practical_salinity
    TW2_2 = TW2*TW2
    TW2_3 = TW2*TW2*TW2
    cW2 = (1449.2 + (4.6 * TW2) - (.055 * TW2_2) + (.00029 * TW2_3) + ((1.34 - 0.01*TW2)*(SW2 - 35)) + (.016*PW2))
    timeW2 = df_W2.time

    PS2=df_S2.seawater_pressure
    TS2=df_S2.seawater_temperature
    SS2=df_S2.practical_salinity
    TS2_2 = TS2*TS2
    TS2_3 = TS2*TS2*TS2
    cS2 = (1449.2 + (4.6 * TS2) - (.055 * TS2_2) + (.00029 * TS2_3) + ((1.34 - 0.01*TS2)*(SS2 - 35)) + (.016*PS2))
    timeS2 = df_S2.time

    yW2 = PW2
    xW2 = cW2
    yS2 = PS2
    xS2 = cS2

# Third data set

    PW3=df_W3.pressure
    TW3=df_W3.temp
    SW3=df_W3.practical_salinity
    TW3_2 = TW3*TW3
    TW3_3 = TW3*TW3*TW3
    cW3 = (1449.2 + (4.6 * TW3) - (.055 * TW3_2) + (.00029 * TW3_3) + ((1.34 - 0.01*TW3)*(SW3 - 35)) + (.016*PW3))
    timeW3 = df_W3.time

    PS3=df_S3.pressure
    TS3=df_S3.temp
    SS3=df_S3.practical_salinity
    TS3_2 = TS3*TS3
    TS3_3 = TS3*TS3*TS3
    cS3 = (1449.2 + (4.6 * TS3) - (.055 * TS3_2) + (.00029 * TS3_3) + ((1.34 - 0.01*TS3)*(SS3 - 35)) + (.016*PS3))
    timeS3 = df_S3.time

    yW3 = PW3
    xW3 = cW3
    yS3 = PS3
    xS3 = cS3

# Fourth data set

    PW4=df_W4.seawater_pressure
    TW4=df_W4.seawater_temperature
    SW4=df_W4.practical_salinity
    TW4_2 = TW4*TW4
    TW4_3 = TW4*TW4*TW4
    cW4 = (1449.2 + (4.6 * TW4) - (.055 * TW4_2) + (.00029 * TW4_3) + ((1.34 - 0.01*TW4)*(SW4 - 35)) + (.016*PW4))
    timeW4 = df_W4.time

    PS4=df_S4.seawater_pressure
    TS4=df_S4.seawater_temperature
    SS4=df_S4.practical_salinity
    TS4_2 = TS4*TS4
    TS4_3 = TS4*TS4*TS4
    cS4 = (1449.2 + (4.6 * TS4) - (.055 * TS4_2) + (.00029 * TS4_3) + ((1.34 - 0.01*TS4)*(SS4 - 35)) + (.016*PS4))
    timeS4 = df_S4.time

    yW4 = PW4
    xW4 = cW4
    yS4 = PS4
    xS4 = cS4


# Fifth data set0   

    PW5=df_W5.pressure
    TW5=df_W5.temp
    SW5=df_W5.practical_salinity
    TW5_2 = TW5*TW5
    TW5_3 = TW5*TW5*TW5
    cW5 = (1449.2 + (4.6 * TW5) - (.055 * TW5_2) + (.00029 * TW5_3) + ((1.34 - 0.01*TW5)*(SW5 - 35)) + (.016*PW5))
    timeW5 = df_W5.time

    PS5=df_S5.pressure
    TS5=df_S5.temp
    SS5=df_S5.practical_salinity
    TS5_2 = TS5*TS5
    TS5_3 = TS5*TS5*TS5
    cS5 = (1449.2 + (4.6 * TS5) - (.055 * TS5_2) + (.00029 * TS5_3) + ((1.34 - 0.01*TS5)*(SS5 - 35)) + (.016*PS5))
    timeS5 = df_S5.time

    yW5 = PW5
    xW5 = cW5
    yS5 = PS5
    xS5 = cS5

# Sixth data set

    PW6=df_W6.seawater_pressure
    TW6=df_W6.seawater_temperature
    SW6=df_W6.practical_salinity
    TW6_2 = TW6*TW6
    TW6_3 = TW6*TW6*TW6
    cW6 = (1449.2 + (4.6 * TW6) - (.055 * TW6_2) + (.00029 * TW6_3) + ((1.34 - 0.01*TW6)*(SW6 - 35)) + (.016*PW6))
    timeW6 = df_W6.time

    PS6=df_S6.seawater_pressure
    TS6=df_S6.seawater_temperature
    SS6=df_S6.practical_salinity
    TS6_2 = TS6*TS6
    TS6_3 = TS6*TS6*TS6
    cS6 = (1449.2 + (4.6 * TS6) - (.055 * TS6_2) + (.00029 * TS6_3) + ((1.34 - 0.01*TS6)*(SS6 - 35)) + (.016*PS6))
    timeS6 = df_S6.time

    yW6 = PW6
    xW6 = cW6
    yS6 = PS6
    xS6 = cS6


# Seventh data set


    PW7=df_W7.pressure
    TW7=df_W7.temp
    SW7=df_W7.practical_salinity
    TW7_2 = TW7*TW7
    TW7_3 = TW7*TW7*TW7
    cW7 = (1449.2 + (4.6 * TW7) - (.055 * TW7_2) + (.00029 * TW7_3) + ((1.34 - 0.01*TW7)*(SW7 - 35)) + (.016*PW7))
    timeW7 = df_W7.time

    PS7=df_S7.pressure
    TS7=df_S7.temp
    SS7=df_S7.practical_salinity
    TS7_2 = TS7*TS7
    TS7_3 = TS7*TS7*TS7
    cS7 = (1449.2 + (4.6 * TS7) - (.055 * TS7_2) + (.00029 * TS7_3) + ((1.34 - 0.01*TS7)*(SS7 - 35)) + (.016*PS7))
    timeS7 = df_S7.time

    yW7 = PW7
    xW7 = cW7
    yS7 = PS7
    xS7 = cS7

# Calculating Number of Dives

# Defining the function

    def diveCount(depth):
    
        bottom = max(depth)
        atBottom = False
        count = 0
 
    
        for i in range(0, len(depth)):
            if(depth[i] > .95*bottom and not atBottom):
                atBottom = True
            
            if(depth[i] < .95*bottom and atBottom):
                atBottom = False
                count += 1
            
        return count

# Number of dives for each data set

    DivesinWinter1 = diveCount(PW1)
    DivesinSummer1 = diveCount(PS1)

    print("The number of dives in Winter (1) is " + str(DivesinWinter1))
    print("The number of dives in Summer (1) is " + str(DivesinSummer1))

    DivesinWinter2 = diveCount(PW2)
    DivesinSummer2 = diveCount(PS2)

    print("The number of dives in Winter (2) is " + str(DivesinWinter2))
    print("The number of dives in Summer (2) is " + str(DivesinSummer2))

    DivesinWinter3 = diveCount(PW3)
    DivesinSummer3 = diveCount(PS3)

    print("The number of dives in Winter (3) is " + str(DivesinWinter3))
    print("The number of dives in Summer (3) is " + str(DivesinSummer3))

    DivesinWinter4 = diveCount(PW4)
    DivesinSummer4 = diveCount(PS4)

    print("The number of dives in Winter (4) is " + str(DivesinWinter4))
    print("The number of dives in Summer (4) is " + str(DivesinSummer4))

    DivesinWinter5 = diveCount(PW5)
    DivesinSummer5 = diveCount(PS5)

    print("The number of dives in Winter (5) is " + str(DivesinWinter5))
    print("The number of dives in Summer (5) is " + str(DivesinSummer5))

    DivesinWinter6 = diveCount(PW6)
    DivesinSummer6 = diveCount(PS6)

    print("The number of dives in Winter (6) is " + str(DivesinWinter6))
    print("The number of dives in Summer (6) is " + str(DivesinSummer6))

    DivesinWinter7 = diveCount(PW7)
    DivesinSummer7 = diveCount(PS7)

    print("The number of dives in Winter (7) is " + str(DivesinWinter7))
    print("The number of dives in Summer (7) is " + str(DivesinSummer7))


# Plotting SSP For Each Dive

# First data set

    def AvgDataSpeed(x,y):
        Depth=y
        Speed=x
        Bottom=max(Depth)
        Output = []
    
        for i in range(0,25):
            Output.append([0.0,0.0,0])
    
        for i in range(0,len(Depth)):
        
            for j in range(0,len(Output)):
            
                if(Depth[i] > (j/25)*Bottom and Depth[i]<((j/25)+.04)*Bottom):
                    Output[j][0]= Output[j][0]+Depth[i]
                    Output[j][1]= Output[j][1]+Speed[i]
                    Output[j][2]+=1
                    break
    
        OutputDepth = []
        OutputSpeed = []
    
        for i in range(0,len(Output)):
            if (Output[i][2]!=0):
                OutputDepth.append(Output[i][0]/Output[i][2])
                OutputSpeed.append(Output[i][1]/Output[i][2])
            
        return OutputDepth , OutputSpeed


    [y1,x1]=AvgDataSpeed(cW1,PW1)

    plt.figure(1)
    plt.scatter(xW1,yW1)
    plt.plot(x1,y1,'r')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Winter1)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    plt.legend()
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])





    [y2,x2]=AvgDataSpeed(cS1,PS1)

    plt.figure(2)
    plt.scatter(xS1,yS1)
    plt.plot(x2,y2,'r')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Summer1)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    plt.legend()
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])


# Second data set

    [y3,x3]=AvgDataSpeed(cW2,PW2)

    plt.figure(3)
    plt.plot(x3,y3, 'r')
    plt.scatter(xW2,yW2)
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Winter2)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])


    [y4,x4]=AvgDataSpeed(cS2,PS2)

    plt.figure(4)
    plt.plot(x4,y4, 'r')
    plt.scatter(xS2,yS2)
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Summer2)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])


# Third data set

    [y5,x5]=AvgDataSpeed(cW3,PW3)

    plt.figure(5)
    plt.plot(x5,y5, 'r')
    plt.scatter(xW3,yW3)
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Winter3)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])

    [y6,x6]=AvgDataSpeed(cS3,PS3)

    plt.figure(6)
    plt.plot(x6,y6, 'r')
    plt.scatter(xS3,yS3)
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Summer3)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])


# Fourth data set

    [y7,x7]=AvgDataSpeed(cW4,PW4)

    plt.figure(7)
    plt.plot(x7,y7, 'r')
    plt.scatter(xW4,yW4)
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Winter4)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])

    [y8,x8]=AvgDataSpeed(cS4,PS4)

    plt.figure(8)
    plt.scatter(xS4,yS4)
    plt.plot(x8,y8, 'r')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Summer4)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])


# Fifth data set

    [y9,x9]=AvgDataSpeed(cW5,PW5)

    plt.figure(9)
    plt.scatter(xW5,yW5)
    plt.plot(x9,y9, 'r')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Winter5)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])

    [y10,x10]=AvgDataSpeed(cS5,PS5)

    plt.figure(10)
    plt.scatter(xS5,yS5)
    plt.plot(x10,y10, 'r')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Summer5)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])


# Sixth data set

    [y11,x11]=AvgDataSpeed(cW6,PW6)

    plt.figure(11)
    plt.scatter(xW6,yW6)
    plt.plot(x11,y11, 'r')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Winter6)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])


    [y12,x12]=AvgDataSpeed(cS6,PS6)


    plt.figure(12)
    plt.scatter(xS6,yS6)
    plt.plot(x12,y12, 'r')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Summer6)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])


# Seventh data set

    [y13,x13]=AvgDataSpeed(cW7,PW7)

    plt.figure(13)
    plt.scatter(xW7,yW7)
    plt.plot(x13,y13, 'r')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Winter7)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])

    [y14,x14]=AvgDataSpeed(cS7,PS7)

    plt.figure(14)
    plt.scatter(xS7,yS7)
    plt.plot(x14,y14, 'r')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Summer7)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    red_patch = mpatches.Patch(color='red', label='Average')
    blue_patch = mpatches.Patch(color='blue', label='ssp')
    plt.legend(handles=[red_patch, blue_patch])


# Finding the Max SSP Value in Each Season

    ssp_Winter=(max(cW1),max(cW2),max(cW3),max(cW4),max(cW5),max(cW6),max(cW7))
    Max_ssp_Winter=max(ssp_Winter)
    print(ssp_Winter)
    print(Max_ssp_Winter)

    

    ssp_Summer=(max(cS1),max(cS2),max(cS3),max(cS4),max(cS5),max(cS6),max(cS7))
    Max_ssp_Summer=max(max(cS1),max(cS2),max(cS3),max(cS4),max(cS5),max(cS6),max(cS7))
    print(ssp_Summer)
    print(Max_ssp_Summer)

#We can see that in Winter, the highest ssp is from cW5, which corresponds to Oregon Slope Base Deep Profiler. In Summer, the highest ssp is from cS2, which is from the Oregon Offshore Cabled Shallow Profiler.

# SSP Profile in Day vs Night

#Since I only chose data from 7am to 7am in Pacific time, day and night can be compared easily by splitting the data evenly in half - 7am to 7pm (day) and 7pm to 7am (night)

    plt.figure(19)
        plt.scatter(timeW1,cW1)
    plt.title('time vs Speed of Sound (Winter1)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(20)
    plt.scatter(timeW2,cW2)
    plt.title('time vs Speed of Sound (Winter2)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(21)
    plt.scatter(timeW3,cW3)
    plt.title('time vs Speed of Sound (Winter3)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(22)
    plt.scatter(timeW4,cW4)
    plt.title('time vs Speed of Sound (Winter4)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(23)
    plt.scatter(timeW5,cW5)
    plt.title('time vs Speed of Sound (Winter5)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(24)
    plt.scatter(timeW6,cW6)
    plt.title('time vs Speed of Sound (Winter6)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')
    
    plt.figure(25)
    plt.scatter(timeW7,cW7)
    plt.title('time vs Speed of Sound (Winter7)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(26)
    plt.scatter(timeS1,cS1)
    plt.title('time vs Speed of Sound (Summer1)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(27)
    plt.scatter(timeS2,cS2)
    plt.title('time vs Speed of Sound (Summer2)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(28)
    plt.scatter(timeS3,cS3)
    plt.title('time vs Speed of Sound (Summer3)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(29)
    plt.scatter(timeS4,cS4)
    plt.title('time vs Speed of Sound (Summer4)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(30)
    plt.scatter(timeS5,cS5)
    plt.title('time vs Speed of Sound (Summer5)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(31)
    plt.scatter(timeS6,cS6)
    plt.title('time vs Speed of Sound (Summer6)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')

    plt.figure(32)
    plt.scatter(timeS7,cS7)
    plt.title('time vs Speed of Sound (Summer7)')
    plt.xlabel('time (s)')
    plt.ylabel('Speed of sound (m/s)')



# SSP Profile in Winter vs Summer

    plt.figure(17)
    plt.plot(xW1,yW1, 'blue')
    plt.plot(xW2,yW2, 'purple')
    plt.plot(xW3,yW3, 'red')
    plt.plot(xW4,yW4, 'green')
    plt.plot(xW5,yW5, 'yellow')
    plt.plot(xW6,yW6, 'cyan')
    plt.plot(xW7,yW7, 'violet')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Winter)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    blue_patch = mpatches.Patch(color='blue', label='1')
    purple_patch = mpatches.Patch(color='purple', label='2')
    red_patch = mpatches.Patch(color='red', label='3')
    green_patch = mpatches.Patch(color='green', label='4')
    yellow_patch = mpatches.Patch(color='yellow', label='5')
    cyan_patch = mpatches.Patch(color='cyan', label='6')
    violet_patch = mpatches.Patch(color='violet', label='7')
    plt.legend(handles=[blue_patch, purple_patch, red_patch, green_patch, yellow_patch, cyan_patch, violet_patch])




    plt.figure(18)
    plt.plot(xS1,yS1, 'blue')
    plt.plot(xS2,yS2, 'purple')
    plt.plot(xS3,yS3, 'red')
    plt.plot(xS4,yS4, 'green')
    plt.plot(xS5,yS5, 'yellow')
    plt.plot(xS6,yS6, 'cyan')
    plt.plot(xS7,yS7, 'violet')
    plt.gca().invert_yaxis()
    plt.title('Depth vs Speed of Sound (Summer)')
    plt.xlabel('Speed of Sound (m/s)')
    plt.ylabel('Depth (m)')
    blue_patch = mpatches.Patch(color='blue', label='1')
    purple_patch = mpatches.Patch(color='purple', label='2')
    red_patch = mpatches.Patch(color='red', label='3')
    green_patch = mpatches.Patch(color='green', label='4')
    yellow_patch = mpatches.Patch(color='yellow', label='5')
    cyan_patch = mpatches.Patch(color='cyan', label='6')
    violet_patch = mpatches.Patch(color='violet', label='7')
    plt.legend(handles=[blue_patch, purple_patch, red_patch, green_patch, yellow_patch, cyan_patch, violet_patch])
