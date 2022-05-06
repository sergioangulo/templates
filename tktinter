from tkinter import Tk
from tkinter.filedialog import askdirectory, askopenfilename
from tkinter import *
from matplotlib.pyplot import text

class MyWindow:
    
    def __init__(self, win):
        self.left_border = 30
        self.text_inputfile_width = 80 
        
        # ROW 1
        ## label
        self.workdir_label=Label(win, text='Ingrese Directorio de trabajo')
        self.workdir_label.place(x=self.left_border, y=50)
        
        ## text input
        self.t1=Entry(bd=3)
        self.t1.config(width=self.text_inputfile_width)
        self.t1.place(x=200, y=50)
        
        ## button search
        self.btn_search_file = Button(win, text="Buscar Directorio", command = self.search_dir)
        self.btn_search_file.place(x=700, y = 47)
        
        # ROW 2
        ## label
        self.param1_lbl=Label(win, text='Ingrese parametro 1')
        self.param1_lbl.place(x=self.left_border, y=100)
        
        ## text inputRR
        self.t2=Entry()
        self.t2.place(x=200, y=100)

        # ROW 3
        ## label
        self.param2_lbl=Label(win, text='Ingrese parametro 2')
        self.param2_lbl.place(x=self.left_border, y=150)
        
        ## text input
        self.t3=Entry()
        self.t3.place(x=200, y=150)
        
        # ROW 4
        self.b1=Button(win, text='Procesar', command=self.procesar)
        self.b1.place(x=self.left_border, y=200)
        
        # ROW 5
        self.status=Label(win, text='')
        self.status.place(x=self.left_border, y=250)
        
    def search_file(self):
        filename = askopenfilename()
        #self.t1.delete(1.0,"end")
        self.t1.insert(END, filename)
    
    def search_dir(self):
        dir = askdirectory()
        #self.t1.delete(1.0,"end")
        self.t1.insert(END, dir)
        
    def procesar(self):
        #self.status.delete(0, 'end')
        texto1=str(self.t1.get())
        parametro1=str(self.t2.get())
        parametro2=str(self.t3.get())
        ## EJECUTA AQUI LA LLAMADA A TU SCRIPT
        result=f"Procesando archivo [{texto1}] con parametros [{parametro1}] y [{parametro2}]\n Aqui va la ejecucion de tu funcion."
        self.status['text'] = str(result) 
        #self.status.insert(END, str(result))
   

window=Tk()
mywin=MyWindow(window)
photo = PhotoImage(file = r"filepath\image.bmp")
window.iconphoto(False, photo)
#window.iconbitmap(r"filepath\image.bmp")
window.title('titulo')
window.geometry("820x300+10+10")
window.mainloop()
