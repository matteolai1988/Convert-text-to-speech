## import libraries

from tkinter import *
from gtts import gTTS
from playsound import playsound



################### Initialized window####################
#pip install playsound==1.2.2

root = Tk()
root.geometry('350x300')
root.resizable(0,0)
root.config(bg='ghost white')
root.title('DataFlair - Make your text speech')


##heading
Label(root, text='TEXT_TO_SPEECH', font='arial 20 bold', bg ='white smoke').pack()
Label(root, text='DataFlair', font='arial 15 bold', bg='white smoke').pack(side=BOTTOM)




#label
Label(root, text ='Enter Text', font ='arial 15 bold', bg ='white smoke').place(x=20,y=60)


##text variable
Msg = StringVar()


#Entry
entry_field = Entry(root,textvariable =Msg, width ='50')
entry_field.place(x=20 , y=100)


###################define function##############################

def Text_to_speech():
    Message = entry_field.get()
    speech = gTTS(text = Message, lang='pl')
    speech.save('SpeakUp.mp3')
    playsound('SpeakUp.mp3')

def Exit():
    root.destroy()

def Reset():
    Msg.set("")

#Button
Button(root, text = "Go" , font = 'arial 15 bold', command = Text_to_speech, width =4).place(x=25, y=140)
Button(root,text = 'Exit',font = 'arial 15 bold' , command = Exit, bg = 'OrangeRed1').place(x=100,y=140)
Button(root, text = 'Reset', font='arial 15 bold', command = Reset).place(x=175 , y =140)


#infinite loop to run program
root.mainloop()
