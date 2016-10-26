package com.quality;

import java.io.*;

/**
 * Created by mykhailo.brodskyi on 10/6/2016.
 */
public class UserDAO {

    final static private String FILENAME = "./README.txt";



    public boolean deleteUser(int id){
        return (id > 10) ? true : false;
    }


    static void writeNumberToFile_0(final int number, final File outputFile)
            throws IOException
    {
        try (FileReader filereader = new FileReader(FILENAME);
             MyReader myreader = new MyReader(filereader)) {
            // do something with myreader
            // ...
        } catch (FileNotFoundException e) {
            System.err.println("testGoodUsage: " + e.getMessage());
        }

        final FileWriter fw = new FileWriter(outputFile);
        fw.write(number);
    }
}

class MyReader extends BufferedReader {

    private Reader m_fr = null;
    public MyReader(Reader in) throws FileNotFoundException {
        super(in);
        m_fr = in;
        throw new FileNotFoundException(
                "Exception in constructor of MyReader ");
    }
}
