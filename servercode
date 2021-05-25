
import java.io.DataInputStream;
import java.io.DataOutputStream;
import java.io.IOException;
import java.io.ObjectInputStream;
import java.net.ServerSocket;
import java.net.Socket;


import org.xml.sax.SAXException;

public class ServerPortal {
	
	public static void main(String args[]) throws IOException, SAXException
    {
		
		// Step 1: Establish the socket connection.
		System.out.println("Sever started");
        ServerSocket ss = new ServerSocket(1777);
        Socket s = ss.accept();
        System.out.println("Connection established");
        
        //DataInputStream dis = new DataInputStream(s.getInputStream());  
		//DataOutputStream dos = new DataOutputStream(s.getOutputStream());
		
		ObjectInputStream ois = new ObjectInputStream(s.getInputStream());
        
        try {
        	
            	// wait for input
        		Object str = ois.readObject();
        	    System.out.println(str);

            }
        catch(Exception e) {
        	System.out.println("Closing connection");
            //s.close();	
            //ss.close();
        }
        
    }
	
}
 


