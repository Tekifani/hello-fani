# hello-fani
Tutorial for github
import java.awt.Button;
import java.awt.Frame;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;


public class ButtonEvent extends Frame implements ActionListener
{
	/**
	 * 
	 */
	private static final long serialVersionUID = 1L;

	private static final Object SOUTH = null;
	private static final Object NORTH = null;
	
	private Button okbtn, cnclbtn;
	
	public ButtonEvent()
	{
		okbtn=new Button("ok");
		okbtn.addActionListener((ActionListener)this);
		add(okbtn,NORTH);


		cnclbtn=new Button("cancel");
		cnclbtn.addActionListener((ActionListener)this);
		add(cnclbtn,SOUTH);
		
		setPreferredSize(getSize());
		setSize(500,500);
		setVisible(true);
		setAlwaysOnTop(true);
		setResizable(true);
	}
	public void actionPerformed(ActionEvent ae)
	{
		Object ob=ae.getActionCommand();
		Object ob1=ae.getSource();
		if(ob1==okbtn)
		{
			System.out.println("Ok button pressed "+ob);
		}
		else
		{
			System.out.println("Cancel button pressed "+ob);
		}
	}
	public static void main(String[] args) 
	{
		new ButtonEvent();
	}

}
