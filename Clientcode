

import java.io.DataInputStream;
import java.io.DataOutputStream;
import java.io.File;
import java.io.IOException;
import java.io.ObjectOutputStream;
import java.net.InetAddress;
import java.net.Socket;

import javax.xml.parsers.DocumentBuilder;
import javax.xml.parsers.DocumentBuilderFactory;
import javax.xml.parsers.ParserConfigurationException;

import org.w3c.dom.Document;
import org.xml.sax.SAXException;

public class ClientPortal {

	public static void main(String[] args) throws IOException, ParserConfigurationException, SAXException {
		InetAddress ip = InetAddress.getLocalHost();
		
		int port = 1777;
		//Scanner sc = new Scanner(System.in);
		
		// Step 1: Open the socket connection.
        Socket s = new Socket(ip, port);
        
        //Communication-get the input and output stream
        //DataInputStream dis = new DataInputStream(s.getInputStream());  
		//DataOutputStream dos = new DataOutputStream(s.getOutputStream());
		
		ObjectOutputStream oos = new ObjectOutputStream(s.getOutputStream());
		
		try {
			
	        	
	        File file = new File("D:\\DataAgumentation\\norwood\\TcpProject\\src\\NewFile.xml");
	        	//an instance of factory that gives a document builder  
	        DocumentBuilderFactory dbf = DocumentBuilderFactory.newInstance();  
	        	//an instance of builder to parse the specified xml file  
	        DocumentBuilder db = dbf.newDocumentBuilder();  
	        Document doc = db.parse(file); 
	        	
	        	//doc.getDocumentElement().normalize(); 
	        	
	        oos.writeObject(doc);
	        System.out.println("After oos");

		}catch(Exception e){
			System.out.println(e);					
		}

	}
	
}
