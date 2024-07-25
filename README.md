# test-case-1

import org.junit.Test;
import static org.junit.Assert.*;

import java.util.HashMap;
import java.util.Map;

public class HashMapTest {

    @Test
    public void testHashMapOperations() {
        // Create a HashMap
        Map<String, Integer> studentScores = new HashMap<>();

        // Add some entries
        studentScores.put("Alice", 95);
        studentScores.put("Bob", 87);
        studentScores.put("Charlie", 92);

        // Test if entries were added correctly
        assertEquals(3, studentScores.size());

        // Test accessing values
        assertEquals(Integer.valueOf(95), studentScores.get("Alice"));
        assertEquals(Integer.valueOf(87), studentScores.get("Bob"));
        assertEquals(Integer.valueOf(92), studentScores.get("Charlie"));

        // Test updating a value
        studentScores.put("Bob", 90);
        assertEquals(Integer.valueOf(90), studentScores.get("Bob"));

        // Test removing an entry
        studentScores.remove("Charlie");
        assertNull(studentScores.get("Charlie"));
        assertEquals(2, studentScores.size());

        // Test clearing the HashMap
        studentScores.clear();
        assertTrue(studentScores.isEmpty());
    }
}
