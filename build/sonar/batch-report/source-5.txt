package com.quality;

import org.junit.Assert;
import org.junit.Test;
import org.junit.runner.RunWith;
import org.junit.runners.JUnit4;

/**
 * Created by mykhailo.brodskyi on 10/6/2016.
 */

@RunWith(JUnit4.class)
public class UserDAOTest {

    @Test
    public void testDeleteUserPositive()
    {
        UserDAO userDAO = new UserDAO();
        Assert.assertTrue(userDAO.deleteUser(11));
        Assert.assertTrue(userDAO.deleteUser(12));

    }

    @Test
    public void testDeleteUserNegative()
    {
        UserDAO userDAO = new UserDAO();
        Assert.assertFalse(userDAO.deleteUser(1));
        Assert.assertFalse(userDAO.deleteUser(2));

    }

    @Test
    public void testDeleteUserNegative2()
    {
        UserDAO userDAO = new UserDAO();
        Assert.assertFalse(userDAO.deleteUser(4));
        Assert.assertFalse(userDAO.deleteUser(5));

    }
    @Test
    public void testDeleteUserNegative3()
    {
        UserDAO userDAO = new UserDAO();
        Assert.assertFalse(userDAO.deleteUser(4));
        Assert.assertFalse(userDAO.deleteUser(5));

    }
}
