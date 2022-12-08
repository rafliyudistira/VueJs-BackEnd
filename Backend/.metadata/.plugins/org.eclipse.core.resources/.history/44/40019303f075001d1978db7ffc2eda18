package com.example.students.repository.impl;

import java.util.List;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.jdbc.core.BeanPropertyRowMapper;
import org.springframework.jdbc.core.JdbcTemplate;
import org.springframework.stereotype.Repository;

import com.example.students.model.Students;
import com.example.students.repository.IStudentsRepository;

@Repository
public class StudentsRepository implements IStudentsRepository {

    @Autowired
    JdbcTemplate jdbcTemplate;

    @Override
    public Students insertStudents(Students students) {
        // TODO Auto-generated method stub
        String query = "INSERT INTO tb_students(nama, umur, jenis_kelamin, deskripsi_diri, email, soft_skill, hard_skill, interest) "
                + "VALUES(?, ?, ?, ?, ?, ?, ?, ?)";
        jdbcTemplate.update(query,
                new Object[] { students.getNama(), students.getUmur(), students.getJenis_kelamin(),
                        students.getDeskripsi_diri(), students.getEmail(), students.getSoft_skill(),
                        students.getHard_skill(),
                        students.getInterest() });
        return students;
    }

    @Override
    public List<Students> getAllStudents() {
        // TODO Auto-generated method stub
        String query = "SELECT * FROM tb_students";
        return jdbcTemplate.query(query, new BeanPropertyRowMapper<>(Students.class));
    }

    @Override
    public Students updateStudents(int id, Students students) {
        // TODO Auto-generated method stub
        String query = "UPDATE tb_students SET nama = ?, umur = ?, jenis_kelamin = ?, deskripsi_diri = ?, "
                + "email = ?, soft_skill = ?, hard_skill = ?, interest = ? WHERE id = ?";

        jdbcTemplate.update(query,
                new Object[] { students.getNama(), students.getUmur(), students.getJenis_kelamin(),
                        students.getDeskripsi_diri(), students.getEmail(), students.getSoft_skill(),
                        students.getHard_skill(),
                        students.getInterest(), id });

        return students;
    }

    @Override
    public Students deleteStudents(int id) {
        // TODO Auto-generated method stub
        String query = "SELECT * FROM tb_students WHERE id = ?";
        var result = jdbcTemplate.queryForObject(query, new BeanPropertyRowMapper<>(Students.class), id);

        query = "DELETE FROM tb_students WHERE id = ?";
        jdbcTemplate.update(query, id);

        return result;
    }

}
